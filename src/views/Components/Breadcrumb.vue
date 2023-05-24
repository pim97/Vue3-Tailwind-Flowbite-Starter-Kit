  
<script setup>
import BreadcrumbItem from '@/views/components/BreadcrumbItem.vue';

const props = defineProps({
    items: {
        type: Array,
        required: true,
    },
});
</script>

<template>
    <nav class="flex px-5 py-3 text-gray-700 border border-gray-200 rounded-lg bg-gray-50 dark:bg-gray-800 dark:border-gray-700"
        aria-label="Breadcrumb">
        <ol class="inline-flex items-center space-x-1 md:space-x-3">
            <BreadcrumbItem v-for="(item, index) in items" :key="index" :icon="item.icon" :item="item" :last="index === items.length - 1" />
        </ol>
    </nav>
</template>
