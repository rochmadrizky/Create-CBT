<template>
  <div
    class="min-h-screen flex items-center justify-center bg-cover"
    :style="{ 'background-image': `url('${backgroundImage}')` }"
  >
    <div class="text-center text-white">
      <h1 class="text-4xl font-bold mb-4">{{ title }}</h1>
      <p class="text-lg mb-6">{{ subtitle }}</p>
      <button
        class="px-6 py-3 bg-blue-500 rounded-full text-white hover:bg-blue-700 transition duration-300"
      >
        {{ buttonText }}
      </button>
    </div>
  </div>
</template>

<script setup>
const props = defineProps([
  "title",
  "subtitle",
  "buttonText",
  "backgroundImage",
]);

const {
  title = "Welcome to Our Website",
  subtitle = "The Best Place to Learn CBT",
  buttonText = "Get Started Now",
  backgroundImage = "https://fastly.picsum.photos/id/43/800/500.jpg?hmac=6B76YRP_2LL-WKYygXItPWUN8qdg4CenBfm4GpgLnzw",
} = props;
</script>
