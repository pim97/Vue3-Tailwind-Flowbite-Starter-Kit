
<script setup>
import Icon from '@/views/components/Icon.vue';

const props = defineProps({
    icon: {
        type: String,
        required: false,
    },
    item: {
        type: Object,
        required: true,
    },
    last: {
        type: Boolean,
        default: false,
    },
});
</script>

<template>
    <li class="inline-flex items-center">
        <a v-if="!last && item.link" :href="item.link"
            class="inline-flex items-center text-sm font-medium text-gray-700 hover:text-blue-600 dark:text-gray-400 dark:hover:text-white">
            
            <Icon :icon="icon" />

            {{ item.label }}

            <svg aria-hidden="true" class="w-6 h-6 text-gray-400" fill="currentColor" viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd"
                    d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                    clip-rule="evenodd"></path>
            </svg>

        </a>

        <span v-else class="inline-flex items-center text-sm font-medium text-gray-700 dark:text-gray-400">

            {{ item.label }}
        </span>
    </li>
</template>
