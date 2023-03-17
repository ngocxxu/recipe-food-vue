<template>
  <div class="h-full bg-gray-100">
    <navbar />
    <main>
      <router-view />
    </main>
  </div>
</template>

<script lang='ts' setup>
import Navbar from './Navbar.vue';

</script>

<style lang="scss" scoped></style>