<template>
  <div class="min-h-screen flex items-center justify-center bg-gray-200">
    <div class="bg-white p-8 rounded shadow-md w-96">
      <h2 class="text-2xl font-semibold mb-4 text-center">Informasi Kontak</h2>

      <div class="mb-4">
        <label for="nama" class="block text-gray-700 text-sm font-bold mb-2"
          >Nama</label
        >
        <input
          v-model="nama"
          type="text"
          id="nama"
          class="w-full p-2 border rounded"
          placeholder="Masukkan nama"
        />
      </div>

      <div class="mb-4">
        <label for="email" class="block text-gray-700 text-sm font-bold mb-2"
          >Email</label
        >
        <input
          v-model="email"
          type="email"
          id="email"
          class="w-full p-2 border rounded"
          placeholder="Masukkan email"
        />
      </div>

      <div class="mb-4">
        <label for="telpon" class="block text-gray-700 text-sm font-bold mb-2"
          >Nomor Telepon</label
        >
        <div class="flex">
          <select
            v-model="pilihanNegara"
            class="w-10 p-2 border rounded appearance-none"
          >
            <option value="us">US</option>
            <option value="sa">SA</option>
            <option value="id">ID</option>
          </select>

          <input
            v-model="telpon"
            type="telpon"
            id="telpon"
            class="w-72 p-2 border rounded"
            :placeholder="`${kodeNegara[pilihanNegara]}`"
            @input="validasiNomer"
          />
        </div>
      </div>

      <div class="mb-4">
        <label
          for="description"
          class="block text-gray-700 text-sm font-bold mb-2"
          >Deskripsi</label
        >
        <textarea
          v-model="deskripsi"
          id="deskripsi"
          class="w-full p-2 border rounded"
          placeholder="Masukkan deskripsi"
        ></textarea>
      </div>

      <button
        @click="tombolKirim"
        class="w-full bg-blue-500 text-white p-2 rounded hover:bg-blue-600"
      >
        Kirim
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const nama = ref("");
const email = ref("");
const pilihanNegara = ref("id");
const telpon = ref("");
const deskripsi = ref("");

const kodeNegara = {
  us: "+1",
  sa: "+966",
  id: "+62",
};

const validasiNomer = () => {
  telpon.value = telpon.value.replace(/\D/g, "");
};

const tombolKirim = () => {
  console.log("Formulir dikirim");
};
</script>
