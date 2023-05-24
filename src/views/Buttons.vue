<script setup>

import Button from '@/views/components/Button.vue';
</script>

<template>
    <div>
        <Button color="blue">Default</Button>
        <Button color="gray" variant="dark">Dark</Button>
        <Button color="gray" variant="light">Light</Button>
        <Button color="green">Green</Button>
        <Button color="red">Red</Button>
        <Button color="yellow">Yellow</Button>
        <Button color="purple">Purple</Button>

        <Button color="blue" gradient>Default Gradient</Button>
        <Button color="gray" gradient variant="dark">Dark Gradient</Button>
        <Button color="gray" gradient variant="light">Light Gradient</Button>
        <Button color="green" gradient>Green Gradient</Button>
        <Button color="red" gradient>Red Gradient</Button>
        <Button color="yellow" gradient>Yellow Gradient</Button>
        <Button color="purple" gradient>Purple Gradient</Button>


        <Button color="blue" rounded>Default Rounded</Button>
        <Button color="gray" rounded variant="dark">Dark Rounded</Button>
        <Button color="gray" rounded variant="light">Light Rounded</Button>
        <Button color="green" rounded>Green Rounded</Button>
        <Button color="red" rounded>Red Rounded</Button>
        <Button color="yellow" rounded>Yellow Rounded</Button>
        <Button color="purple" rounded>Purple Rounded</Button>

        <Button color="blue" gradient rounded>Default Gradient Rounded</Button>
        <Button color="gray" gradient rounded variant="dark">Dark Gradient Rounded</Button>
        <Button color="gray" gradient rounded variant="light">Light Gradient Rounded</Button>
        <Button color="green" gradient rounded>Green Gradient Rounded</Button>
        <Button color="red" gradient rounded>Red Gradient Rounded</Button>
        <Button color="yellow" gradient rounded>Yellow Gradient Rounded</Button>
        <Button color="purple" gradient rounded>Purple Gradient Rounded</Button>

        <Button color="blue" shadow>Default Shadow</Button>
        <Button color="gray" shadow variant="dark">Dark Shadow</Button>
        <Button color="gray" shadow variant="light">Light Shadow</Button>
        <Button color="green" shadow>Green Shadow</Button>
        <Button color="red" shadow>Red Shadow</Button>
        <Button color="yellow" shadow>Yellow Shadow</Button>
        <Button color="purple" shadow>Purple Shadow</Button>

        <Button color="blue" gradient shadow>Default Gradient Shadow</Button>
        <Button color="gray" gradient shadow variant="dark">Dark Gradient Shadow</Button>
        <Button color="gray" gradient shadow variant="light">Light Gradient Shadow</Button>
        <Button color="green" gradient shadow>Green Gradient Shadow</Button>
        <Button color="red" gradient shadow>Red Gradient Shadow</Button>
        <Button color="yellow" gradient shadow>Yellow Gradient Shadow</Button>
        <Button color="purple" gradient shadow>Purple Gradient Shadow</Button>

        <Button color="blue" rounded shadow>Default Rounded Shadow</Button>
        <Button color="gray" rounded shadow variant="dark">Dark Rounded Shadow</Button>
        <Button color="gray" rounded shadow variant="light">Light Rounded Shadow</Button>
        <Button color="green" rounded shadow>Green Rounded Shadow</Button>
        <Button color="red" rounded shadow>Red Rounded Shadow</Button>
        <Button color="yellow" rounded shadow>Yellow Rounded Shadow</Button>
        <Button color="purple" rounded shadow>Purple Rounded Shadow</Button>

        <Button color="blue" gradient rounded shadow>Default Gradient Rounded Shadow</Button>
        <Button color="gray" gradient rounded shadow variant="dark">Dark Gradient Rounded Shadow</Button>
        <Button color="gray" gradient rounded shadow variant="light">Light Gradient Rounded Shadow</Button>
        <Button color="green" gradient rounded shadow>Green Gradient Rounded Shadow</Button>
        <Button color="red" gradient rounded shadow>Red Gradient Rounded Shadow</Button>
        <Button color="yellow" gradient rounded shadow>Yellow Gradient Rounded Shadow</Button>
        <Button color="purple" gradient rounded shadow>Purple Gradient Rounded Shadow</Button>

        <Button color="blue" gradient :gradient-colors="['blue-500', 'yellow-700']">Blue Gradient</Button>
        <Button color="red" rounded>Red Rounded</Button>
        <Button color="green" size="lg" shadow>Large Green with Shadow</Button>


    </div>
</template>

  
<style scoped></style>