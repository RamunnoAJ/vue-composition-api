<template>
  <div class="home">

    <h2>{{ appTitle }}</h2>
    <h3>{{ counterData.title }}:</h3>

    <div>
      <button @click="decreaseCounter" class="btn">-</button>
      <span class="counter">{{ counterData.count }}</span>
      <button @click="increaseCounter" class="btn">+</button>
    </div>

    <div class="edit">
      <h4>Edit counter title:</h4>
      <input v-model="counterData.title" type="text">
    </div>

  </div>
</template>

<script setup>
import { onMounted, reactive } from 'vue';

const appTitle = 'My Amazing Counter App'

onMounted(() => {
  console.log('do stuff related to App title')
})

const counterData = reactive({
  count: 0,
  title: 'My Counter'
})

const increaseCounter = () => {
  counterData.count++
}

const decreaseCounter = () => {
  counterData.count--
}

onMounted(() => {
  console.log('do stuff related to Counter')
})

// onBeforeMount(() => {
//   console.log('onBeforeMount')
// })

// onMounted(() => {
//   console.log('onMounted')
// })

// onBeforeUnmount(() => {
//   console.log('onBeforeUnmount')
// })

// onUnmounted(() => {
//   console.log('onUnmounted')
// })

// onActivated(() => {
//   console.log('onActivated')
// })

// onDeactivated(() => {
//   console.log('onDeactivated')
// })

// onBeforeUpdate(() => {
//   console.log('onBeforeUpdate')
// })

// onUpdated(() => {
//   console.log('onUpdated')
// })
</script>


<style>
.home {
  text-align: center;
  padding: 20px;
}

.btn,
.counter {
  font-size: 40px;
  margin: 10px;
}

.edit {
  margin-top: 60px;
}
</style>