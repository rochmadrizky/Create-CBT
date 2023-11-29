<template>
  <ul class="flex flex-col lg:flex-row lg:space-x-7">
    <li class="mb-8 ml-3 lg:mb-0">
      <NuxtLink
        to="/"
        @click="$emit(`onMenuClick`)"
        class="font-first md:text-xl"
        >Regards!</NuxtLink
      >
    </li>
    <li class="mb-8 ml-3 lg:mb-0">
      <NuxtLink
        to="/about-us"
        @click="$emit(`onMenuClick`)"
        class="font-first md:text-xl"
        >About</NuxtLink
      >
    </li>
    <li class="mb-8 ml-3 lg:mb-0">
      <NuxtLink
        to="/clients-us"
        @click="$emit(`onMenuClick`)"
        class="font-first md:text-xl"
        >Clients</NuxtLink
      >
    </li>
    <li class="mb-8 ml-3 lg:mb-0">
      <NuxtLink
        to="/contact-us"
        @click="$emit(`onMenuClick`)"
        class="font-first md:text-xl"
        >Contact Us</NuxtLink
      >
    </li>
    <li class="mb-8 ml-3 lg:mb-0">
      <NuxtLink
        to="/fetch-data"
        @click="$emit(`onMenuClick`)"
        class="font-first md:text-xl"
        >Fecth Data</NuxtLink
      >
    </li>
  </ul>
</template>

<script setup>
defineEmits(["onMenuClick"]);
</script>
