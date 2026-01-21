<script setup>
    import { ref } from 'vue';

    let message = ref('I need help'); //Ref updateib kõike, mis kasutab seda kui see muutub

    function input(event)
    {
        console.log(event.target.value);
        message.value = event.target.value;
    }
</script>

<template>
    <div class="container">
        <h1>{{ message }}</h1>
        <button class="button is primary" v-on:click="message = 'I need sleep!'">Click me!</button>
        <input class="input" v-bind:value="message" v-on:input="input">
    </div>
</template>

<style>

</style>