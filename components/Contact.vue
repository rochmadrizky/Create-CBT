<template>
  <div class="mt-5 flex items-center justify-center">
    <div
      class="bg-gray-100 bg-opacity-50 opacity-95 p-8 rounded shadow-md w-96"
    >
      <div>
        <div class="mb-4">
          <label for="nama" class="block text-sm font-bold mb-2">Name</label>
          <input
            v-model="nama"
            type="text"
            id="nama"
            class="w-full p-2 border rounded"
            placeholder="Enter your name"
          />
        </div>

        <div class="mb-4">
          <label for="email" class="block text-sm font-bold mb-2">Email</label>
          <input
            v-model="email"
            type="email"
            id="email"
            class="w-full p-2 border rounded"
            placeholder="Enter your email"
          />
        </div>

        <div class="mb-4">
          <label for="telpon" class="block text-sm font-bold mb-2"
            >Phone number</label
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
          <label for="deskripsi" class="block text-sm font-bold mb-2"
            >Description</label
          >
          <textarea
            v-model="deskripsi"
            id="deskripsi"
            class="w-full p-2 border rounded"
            placeholder="Add a short description"
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
