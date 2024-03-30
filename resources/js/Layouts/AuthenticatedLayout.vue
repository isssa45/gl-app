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
    <div class="h-full  bg-blue-300">
        <!-- flex -->
        <div class="flex items-center h-[88px] py-8 px-8 w-full fixed z-50 justify-between bg-white">
             <img class="h-12" src="assets/logo.svg" alt="">
             <Navbar class="flex mx-[180px]"/>
             <div class="flex">
                <Notification class="mr-3" />
                <div class="bg-green-400 rounded-full w-12 h-12 mr-3"></div>
                <button class="bg-indigo-500 py-3 px-6 text-white rounded-lg">Post a Job</button>
             </div>
        </div>
    </div>

    <!-- <main class="pt-[88px]">
        <slot />
    </main> -->

    <main class="">
        <!-- w-full mx-auto -->
            <div class="pt-[88px]"></div>
            <slot />
        </main>
    <!-- <h6 class="w-full bg-slate-100 h-12 ">2222ss</h6> -->
    <footer class="bg-indigo-500">
            <div class="bg-indigo-800 hover:bg-indogo-600 w-full p-3.5 cursor-pointer text-white font-extrabold text-center">
                Retour vers le Haut
            </div>
            <div class="flex items-stretch justify-between max-w-[1200px] mx-auto p-10 text-white">
                <ul>
                    <li class="font-extrabold text-lg">Découvrir des Opportunités</li>
                    <li class="hover:underline cursor-pointer">Stages</li>
                    <li class="hover:underline cursor-pointer">Postes pour Débutants</li>
                    <li class="hover:underline cursor-pointer">Programmes de Diplômés</li>
                    <li class="hover:underline cursor-pointer">Postes de Recherche</li>
                    <li class="hover:underline cursor-pointer">Emplois à l'Étranger</li>
                    <li class="hover:underline cursor-pointer">Alternance</li>
                </ul>

                <ul>
                    <li class="font-extrabold text-lg">Ressources</li>
                    <li class="hover:underline cursor-pointer">Conseils pour CV</li>
                    <li class="hover:underline cursor-pointer">Préparation aux Entretiens</li>
                    <li class="hover:underline cursor-pointer">Conseils de Réseautage</li>
                    <li class="hover:underline cursor-pointer">Salons de l'emploi</li>
                    <li class="hover:underline cursor-pointer">Articles et Guides</li>
                    <li class="hover:underline cursor-pointer">Vidéos de Conseils Carrière</li>
                </ul>

                <ul>
                    <li class="font-extrabold text-lg">Nous Contacter</li>
                    <li class="hover:underline cursor-pointer">Contact</li>
                    <li class="hover:underline cursor-pointer">FAQ</li>
                    <li class="hover:underline cursor-pointer">À Propos de Nous</li>
                    <li class="hover:underline cursor-pointer">Politique de Confidentialité</li>
                    <li class="hover:underline cursor-pointer">Support Technique</li>
                    <li class="hover:underline cursor-pointer">Signaler un Problème</li>
                </ul>

                <ul>
                    <li class="font-extrabold text-lg">Suivez-nous</li>
                    <li class="hover:underline cursor-pointer">LinkedIn</li>
                    <li class="hover:underline cursor-pointer">Twitter</li>
                    <li class="hover:underline cursor-pointer">Instagram</li>
                    <li class="hover:underline cursor-pointer">Facebook</li>
                    <li class="hover:underline cursor-pointer">YouTube</li>
                    <li class="hover:underline cursor-pointer">Pinterest</li>
                </ul>
            </div>
        </footer>
</template>

<script>

</script>
