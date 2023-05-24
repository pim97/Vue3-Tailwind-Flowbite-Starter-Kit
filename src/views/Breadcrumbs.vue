<script setup>
import Breadcrumb from '@/views/components/Breadcrumb.vue';
import { computed } from 'vue';
import { BeakerIcon } from '@heroicons/vue/24/solid'

const items =  [
    { label: 'Home', link: '/' },
    { label: 'Templates', link: '/templates', icon: BeakerIcon },
    { label: 'Flowbite' },
]
</script>

<template>
    <div>
        <Breadcrumb :items="items" />
    </div>
</template>
