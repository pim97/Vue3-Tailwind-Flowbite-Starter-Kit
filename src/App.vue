<script setup>
import TreeShaking from './views/components/TreeShaking.vue';


</script>

<template>
    <router-view />

    <!-- Prevent Tree Shaking -->
    <TreeShaking></TreeShaking>

</template>

