<template>
  <ul class="menu relative">
    <div class="menu-indicator 
    absolute h-1 bottom-0 
    left-0 m-auto w-12 bg-indigo-400 
    transition-all ease duration-500s
    "
    :style="{left: positionToMove, width: sliderWidth}"
    >
    </div>
    <li class="menu-item" v-for="link in links" :key="link.id" @click="sliderIndicator(link.id)" :ref="'menu-item_'+link.id" >
      <a href="#" class="menu-link flex px-3 py-4 text-slate-300 items-center h-[88px]"
      :class="link.id=== selectedIndex ? 'active':null"
      >
        <font-awesome-icon class="menu-icon h-6 w-6 justify-center items-center inline-flex mr-2" :icon="link.icon"/> 
        <span class="text-base">{{ link.text  }}</span> 
      </a>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      sliderPosition:0,
      selectedElementWidth:0,
      selectedIndex: 0,
      links: [{
      id:1,
      icon: 'fa-solid fa-house',
      text: 'Home'
      },{
      id:2,
      icon: 'fa-solid fa-briefcase',
      text:  'Find Jobs'
      },
      {
      id:3,
      icon: 'fa-solid fa-clipboard-list',
      text: 'My Jobs'
      },
      {
      id:4,
      icon: 'fa-solid fa-bookmark',
      text: 'Saved'
      },
      {
      id:5,
      icon: 'fa-solid fa-envelope-open-text',
      text: 'Messages'
      }],
    }
  },
  methods:{
    sliderIndicator(id){
      // console.log(id); 
      // console.log(this.$refs);
      //this.$refs return object of objects 
      let el= this.$refs[`menu-item_${id}`][0];
      // console.log(el);
      this.sliderPosition = el.offsetLeft;
      // console.log(this.sliderPosition);
      this.selectedElementWidth = el.offsetWidth;
      this.selectedIndex = id;
      // console.log(this.selectedIndex);
      // console.log(this.selectedElementWidth)
    }
  },
  computed:{
    positionToMove(){
      return this.sliderPosition +"px";
    },
    sliderWidth(){
      return this.selectedElementWidth +"px";
    }
  }
}
// import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
</script>

<style lang="scss" scoped>
  .menu-link:hover,.menu-link.active{
    color: #818cf8;
  }
  span:hover,.active > span {
    color: #1e1b4b;
  }
</style>



<!-- 

-----------------------------NOTES--------------------------------------------
------------------------------------------------------------------------------
console.log(this.$refs);  
  
Given object
const obj = {
    "menu-item_1": [{}],
    "menu-item_2": [{}],
    "menu-item_3": [{}],
    "menu-item_4": [{}],
    "menu-item_5": [{}]
};

// Accessing the content of array in item3
const menuItem3Content = obj["menu-item_3"];

// Now you can access the content of the array
console.log(menuItem3Content);

// Accessing the first element of the array inside menu-item_3
const firstElementOfMenuItem3 = obj["menu-item_3"][0];

// Now you can access properties of the first element
console.log(firstElementOfMenuItem3);

obj["menu-item_3"]: This part accesses a property from the object obj. In JavaScript,
there are two ways to access properties of an object: dot notation (obj.propertyName) and bracket notation (obj["propertyName"]). 
In this case, since the property name contains a hyphen (-), 
which isn't valid for dot notation, we're using bracket notation. -->










<!-- 
---------------------trash---------------------
-------------------
  <template>
 <ul class="menu">
              <div class="menu-indicator">
                  <li class="menu-item" v-for="link in links" :key="link.id" >
                      <a href="" class="menu-link">
                        <i class="menu-icon"  :class="link.icon"></i>
                        <span>{{ link.text }}</span>
                      </a>
                  </li>
              </div>
            </ul>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

export default {
  data(){
    return {
    sliderPosition:0,
    selectedElementWidth:0,
    selctedIndex:0,
//     links:[
//       {
//       id:1,
//       icon: 'fa-solid fa-house',
//       text: 'Home'
//       },{
//       id:2,
//       icon: 'fa-solid fa-briefcase',
//       text:  'Find Jobs'
//       },
//       {
//       id:3,
//       icon: 'fa-solid fa-clipboard-list',
//       text: 'My Jobs'
//       },
//       {
//       id:4,
//       icon: 'fa-solid fa-bookmark',
//       text: 'Saved'
//       },
//       {
//       id:5,
//       icon: 'fa-solid fa-envelope-open-text',
//       text: 'Messages'
//       },
//   ],
    }
  }
};

</script>

<style scoped>

</style> -->


