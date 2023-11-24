<template>
  <div
    class="min-h-[35vh] flex items-center justify-center bg-cover bg-top"
    style="
      background-image: url('https://fastly.picsum.photos/id/43/800/500.jpg?hmac=6B76YRP_2LL-WKYygXItPWUN8qdg4CenBfm4GpgLnzw');
    "
  >
    <div>
      <div class="py-8">
        <h1 class="text-3xl text-white text-center">About Us,</h1>
        <p class="font-light text-lg text-white text-center">
          let's get to know us in more detail.
        </p>
        <p class="font-light text-lg text-white text-center">
          about what features we provide.
        </p>
      </div>

      <div class="py-5">
        <About />
      </div>
    </div>
  </div>
  <div class="py-14">
    <h1 class="text-3xl text-center">Starting with price,</h1>
    <p class="font-light text-lg text-center">
      has features that are very helpful for your event.
    </p>
    <PriceCard />
    <p class="font-light text-lg text-center">
      find the best options for your event here.
    </p>
  </div>
</template>

<script setup></script>
