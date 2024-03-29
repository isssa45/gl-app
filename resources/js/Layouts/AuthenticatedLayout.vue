<script setup>
import { ref } from 'vue';
import ApplicationLogo from '@/Components/ApplicationLogo.vue';
import Dropdown from '@/Components/Dropdown.vue';
import DropdownLink from '@/Components/DropdownLink.vue';
import NavLink from '@/Components/NavLink.vue';
import Navbar from '@/Components/Navbar.vue';
import Notification from '@/Components/Notification.vue'
import ResponsiveNavLink from '@/Components/ResponsiveNavLink.vue';
import { Link } from '@inertiajs/vue3'; 
import { list } from 'postcss';

const showingNavigationDropdown = ref(false);
</script>

<template>
    <div class="min-w-[1440px] h-full bg-gray-200 flex">
        <div class="flex items-center h-[88px] py-8 mx-8 fixed z-50 min-w-[1440px] w-full">
             <img class="h-12" src="assets/logo.svg" alt="">
             <Navbar class="flex mx-[180px]"/>
             <Notification />
        </div>
        <div class="flex items-center">
            
        </div>
    </div>
</template>

<script>

</script>
