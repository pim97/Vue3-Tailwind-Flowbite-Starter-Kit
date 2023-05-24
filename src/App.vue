<script setup>
import TreeShaking from './views/Components/TreeShaking.vue';


</script>

<template>
    <router-view />

    <!-- Prevent Tree Shaking -->
    <TreeShaking></TreeShaking>

</template>

