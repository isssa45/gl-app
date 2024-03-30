<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';



</script>

<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <div class="bg-red-400 min-h-[500px]">
            here is the content of the page
        </div>
    </AuthenticatedLayout>

</template>
