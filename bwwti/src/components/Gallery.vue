<template>
  <div class="max-w-6xl mx-auto p-6">
    <h1 class="text-4xl font-bold text-center mb-6">Art Gallery</h1>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
      <div v-for="art in artwork" :key="art.id" class="bg-white rounded-lg shadow-md overflow-hidden">
        <img :src="art.image" :alt="art.name" class="w-full h-48 object-cover">
        <div class="p-4">
          <h2 class="text-lg font-semibold">{{ art.name }}</h2>
          <p class="text-gray-600">{{ art.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import MonaLisa from '@/assets/MonaLisa.jpg';
import StarryNight from '@/assets/StarryNight.jpg';
import GirlWithThePearlEarring from '@/assets/GirlWithThePearlEarring.jpg';
import TheScream from '@/assets/TheScream.jpg';

export default {
  name: "Gallery",
  data() {
    return {
      artwork: [
        { id: 1, name: "Mona Lisa", image: MonaLisa, description: "A renoun painting by Leonardo Da Vinci from the the Renaissance in the 1500's depicting a portrait of a french wife." },
        { id: 2, name: "Starry Night", image: StarryNight, description: "An oil painting from 1889 by Vincent van Gogh of the view from his an asylum using one of the most famous brushstrokes." },
        { id: 3, name: "Girl with the Pearl Earring", image: GirlWithThePearlEarring, description: "A tronie painting done by Johannes Vermeer in 1665 renoun for its detail, lighting, and spacing." },
        { id: 4, name: "The Scream", image: TheScream, description: "Painted by Edvard Munch in 1893 dipicting an abstract depiction of panic and fear." },
      ]
    };
  }
};
</script>

<style scoped>
img {
  height: 15em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
</style>
