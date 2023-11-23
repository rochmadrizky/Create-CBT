<template>
  <div class="max-w-4xl mx-auto mt-10 flex items-center justify-center">
    <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
      <a
        v-for="client in clients"
        :key="client.id"
        :href="client.website"
        target="_blank"
        rel="noopener noreferrer"
        class="mb-6"
      >
        <div
          class="flex flex-col items-center bg-gray-100 rounded-lg pb-4 relative aspect-square"
        >
          <img
            :src="client.logo"
            alt="Logo Klien"
            class="w-14 h-14 rounded-full mb-2 -top-6 absolute"
          />
          <div class="text-center pt-10 px-4">
            <h3 class="text-lg font-semibold">{{ client.name }}</h3>
            <p class="text-sm">{{ client.description }}</p>
          </div>
        </div>
      </a>
    </div>
  </div>
</template>

<script setup>
const clients = [
  {
    id: 1,
    name: "Client A",
    description: "Providing innovative solutions asasasasasasasasa.",
    logo: "https://fastly.picsum.photos/id/695/100/100.jpg?hmac=LIezvpKBefTVd40j2QvE0-wZHjbNkd3MibjENyFCDEQ",
    website: "https://www.client-a.com",
  },
  {
    id: 2,
    name: "Client B",
    description: "Leaders in technology and design.",
    logo: "https://fastly.picsum.photos/id/695/100/100.jpg?hmac=LIezvpKBefTVd40j2QvE0-wZHjbNkd3MibjENyFCDEQ",
    website: "https://www.client-b.com",
  },
  {
    id: 3,
    name: "Client C",
    description: "Leaders in technology and design.",
    logo: "https://fastly.picsum.photos/id/695/100/100.jpg?hmac=LIezvpKBefTVd40j2QvE0-wZHjbNkd3MibjENyFCDEQ",
    website: "https://www.client-b.com",
  },
  {
    id: 4,
    name: "Client D",
    description: "Leaders in technology and design.",
    logo: "https://fastly.picsum.photos/id/695/100/100.jpg?hmac=LIezvpKBefTVd40j2QvE0-wZHjbNkd3MibjENyFCDEQ",
    website: "https://www.client-b.com",
  },
  {
    id: 5,
    name: "Client E",
    description: "Leaders in technology and design.",
    logo: "https://fastly.picsum.photos/id/695/100/100.jpg?hmac=LIezvpKBefTVd40j2QvE0-wZHjbNkd3MibjENyFCDEQ",
    website: "https://www.client-b.com",
  },
  {
    id: 6,
    name: "Client F",
    description: "Leaders in technology and design.",
    logo: "https://fastly.picsum.photos/id/695/100/100.jpg?hmac=LIezvpKBefTVd40j2QvE0-wZHjbNkd3MibjENyFCDEQ",
    website: "https://www.client-b.com",
  },
];
</script>
