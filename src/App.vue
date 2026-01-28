<script setup>
import { ref } from 'vue';
 
let modal1Active = ref(false);
 
</script>
 
<template>
    <div class="container">
      <button class="button is-primary" @click="modal1Active=true">Open modal</button>
        <div :class="modal1Active ? 'modal is-active' : 'modal'">
            <div class="modal-background" @click="modal1Active=false"></div>
            <div class="modal-content">
                <p class="image is-4by3">
                    <img src="https://bulma.io/assets/images/placeholders/1280x960.png" alt="">
                </p>
            </div>
            <button class="modal-close is-large" aria-label="close" @click="modal1Active=false"></button>
        </div>
    </div>
</template>
 
<style></style>