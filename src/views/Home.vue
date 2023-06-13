<template>
  <div>
    <input
      type="text"
      class="rounded border-2 border-gray-200"
      placeholder="Search meal by name"
    />
    <div>
      <router-link to="/" v-for="letter of letters">{{ letter }}</router-link>
    </div>
  </div>
</template>

<script setup>
import { computed } from "vue";
import store from "../store";

const meals = computed(() => store.state.meals);
const letters = "ABCDEFJHIJKLMNOPQRSTUWXYZ".split("");
</script>
