<script setup>
import HelloWorld from './components/HelloWorld.vue'
import { ref } from 'vue'
const eggCount = ref(0)
const tortillaCount = ref(0)
const chocolateCount = ref(0)
</script>

<template>
  <div class="content">
    <a>
      <img src="./assets/eggs.jpg" class="Eggs" alt="a carton of eggs." />
    </a>
  
    <div class="card">
      <button type="button" @click="eggCount--"> - </button>
      <span>{{ eggCount }}</span>
      <button type="button" @click="eggCount++"> +{{ count }}</button>
    </div>

    <a>
      <img src="./assets/tortillas.jpg" class="Tortillas" alt="a bag of tortillas" />
    </a>
    <div class="card">
      <button type="button" @click="tortillaCount--"> - </button>
      <span>{{ tortillaCount }}</span>
      <button type="button" @click="tortillaCount++"> +{{ count }}</button>
    </div>

    <a>
      <img src="./assets/chocolate.jpg" class="Chocolate" alt="a chocolate bar" />
    </a>
    <div class="card">
    <button type="button" @click="chocolateCount--"> - </button>
    <span>{{ chocolateCount }}</span>
    <button type="button" @click="chocolateCount++"> +{{ count }}</button>
  </div>
  </div>
  <HelloWorld msg="" />
</template>

<style scoped>
.Eggs, .Tortillas, .Chocolate {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.card {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1em;
  margin: 1em;
  border: 2px solid #000;
  border-radius: 4px;
}

</style>
