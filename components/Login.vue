<template>
  <div class="min-h-screen flex items-center justify-center bg-gray-200">
    <div class="bg-white p-8 rounded shadow-md w-96">
      <h2 class="text-2xl font-semibold mb-4">Login CBT</h2>

      <div class="mb-4">
        <label for="email" class="block text-gray-700 text-sm font-bold mb-2"
          >Email</label
        >
        <input
          v-model="email"
          type="text"
          id="email"
          class="w-full p-2 border rounded"
          placeholder="Masukan email dulu"
        />
      </div>

      <div class="mb-4">
        <label for="password" class="block text-gray-700 text-sm font-bold mb-2"
          >Password</label
        >
        <div class="relative">
          <input
            v-model="password"
            :type="tampilkanPassword ? 'text' : 'password'"
            id="password"
            class="w-full p-2 border rounded"
            :placeholder="tampilkanPassword ? 'Masukan password' : '*********'"
          />
          <button
            @click="tombolTampilkanPassword"
            class="absolute top-0 right-0 mt-2 mr-3 text-sm text-blue-500 cursor-pointer focus:outline-none"
          >
            {{ tampilkanPassword ? "Sembunyikan" : "Tampilkan" }}
          </button>
        </div>
      </div>

      <button
        @click="login"
        class="w-full bg-blue-500 text-white p-2 rounded hover:bg-blue-600"
      >
        Login
      </button>

      <p class="mt-4 text-blue-500">
        <span class="font-semibold text-black">Note:</span>
        Silahkan login dahulu gaes untuk memulai ujian, Semoga sukses dan diberi
        kelancaran yaa:)
      </p>
    </div>
  </div>
</template>

<script setup>
const email = ref("");
const password = ref("");
const tampilkanPassword = ref(false);

const tombolTampilkanPassword = () => {
  tampilkanPassword.value = !tampilkanPassword.value;
};

const login = () => {
  console.log("coba tombol");
};
</script>
