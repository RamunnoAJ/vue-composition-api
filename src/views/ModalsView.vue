<template>
  <div class="modals">
    <h1>Modals</h1>
    <button @click="showModal = true">Show modal</button>

    <teleport to=".modals-container">
      <div class="modal" v-if="showModal">
        <h1>This is a modal</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati ut quisquam quidem accusamus, dolorem
          fugit
          rem minima voluptatem eaque mollitia necessitatibus dolores, numquam omnis quibusdam eius corrupti perferendis
          dolorum. Maxime.</p>
        <button @click="showModal = false">Hide modal</button>
      </div>
    </teleport>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const showModal = ref(false)
</script>

<style>
.modal {
  background: beige;
  padding: 10px;
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
}

.modal p,
.modal h1 {
  color: black;
}
</style>