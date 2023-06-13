<template>
  <div>
    <input
      type="text"
      class="rounded border-2 border-gray-200"
      placeholder="Search meal by name"
    />
    <div>
      <router-link
        v-for="letter of letters"
        :key="letter"
        :to="{ name: 'byLetter', params: { letter } }"
        >{{ letter }}
      </router-link>
    </div>
  </div>
</template>

<script setup>
import { computed, onMounted } from "vue";

import store from "../store";
import axiosClient from "../axiosClient.js";

const letters = "ABCDEFJHIJKLMNOPQRSTUWXYZ".split("");

onMounted(async () => {
  const response = await axiosClient.get("/list.php?i=list");
  console.log(response.data);
});
</script>
