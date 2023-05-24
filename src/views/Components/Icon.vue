<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    icon: {
        type: Object,
        required: false,
    },
    width: {
        type: Number,
        default: 5,
        required: false,
    },
    height: {
        type: Number,
        default: 5,
        required: false,
    }
});
</script>

<template>
    <div>
        <span v-if="icon" class="icon">
            <component :is="icon" :class="`w-${width} h-${height}`" />
        </span>
    </div>
</template>
  
 