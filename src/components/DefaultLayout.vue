<template>
  <div>
    <MenuBar />
    <main>
      <div class="max-w-[1200px] mx-auto">
        <router-view />
      </div>
    </main>
  </div>
</template>

<script setup>
import MenuBar from "./MenuBar.vue";
</script>
