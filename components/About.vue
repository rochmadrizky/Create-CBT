<template>
  <div class="max-w-4xl mx-auto mt-10 flex items-center justify-center">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
      <div v-for="client in clients" :key="client.id" class="mb-2">
        <div
          class="flex flex-col items-center bg-gray-100 bg-opacity-70 rounded-lg"
        >
          <img
            :src="client.logo"
            alt="Logo Klien"
            class="w-20 h-20 rounded-full mt-5"
          />
          <div class="text-center p-6">
            <h3 class="text-lg font-semibold">{{ client.name }}</h3>
            <p class="text-sm">{{ client.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const clients = [
  {
    id: 1,
    name: "Fitur 1",
    description:
      "Lorem satu dua tiga empat lima enam tujuh delapan sembilan sepuluh",
    logo: "https://fastly.picsum.photos/id/695/100/100.jpg?hmac=LIezvpKBefTVd40j2QvE0-wZHjbNkd3MibjENyFCDEQ",
  },
  {
    id: 2,
    name: "Fitur 2",
    description:
      "Lorem satu dua tiga empat lima enam tujuh delapan sembilan sepuluh",
    logo: "https://fastly.picsum.photos/id/695/100/100.jpg?hmac=LIezvpKBefTVd40j2QvE0-wZHjbNkd3MibjENyFCDEQ",
  },
  {
    id: 3,
    name: "Fitur 3",
    description:
      "Lorem satu dua tiga empat lima enam tujuh delapan sembilan sepuluh",
    logo: "https://fastly.picsum.photos/id/695/100/100.jpg?hmac=LIezvpKBefTVd40j2QvE0-wZHjbNkd3MibjENyFCDEQ",
  },
  {
    id: 4,
    name: "Fitur 4",
    description:
      "Lorem satu dua tiga empat lima enam tujuh delapan sembilan sepuluh",
    logo: "https://fastly.picsum.photos/id/695/100/100.jpg?hmac=LIezvpKBefTVd40j2QvE0-wZHjbNkd3MibjENyFCDEQ",
  },
];
</script>
