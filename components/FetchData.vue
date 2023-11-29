<template>
  <div>
    <h1 class="text-2xl font-bold mb-4">Fetch data pengguna:</h1>
    <ul>
      <li v-for="data in pengguna" :key="data.id" class="mb-2">
        <p>nama: {{ data.name }}</p>
        <p>email: {{ data.email }}</p>
        <p>phone: {{ data.phone }}</p>
      </li>
    </ul>
  </div>
</template>

<script setup>
const pengguna = ref([]);

const fetchData = () => {
  fetch("https://jsonplaceholder.typicode.com/users")
    .then((response) => response.json())
    .then((json) => {
      pengguna.value = json;
    })
    .catch((error) => console.error("Error fetching data:", error));
};

onMounted(() => {
  fetchData();
});
</script>
