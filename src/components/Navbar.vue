<template>
  <header class="bg-white shadow h-16 flex justify-between items-stretch">
    <router-link class="inline-flex items-center h-full px-5" to="/">
      Home
    </router-link>
    <div class="flex items-center gap-1">
      <router-link :to="`/by-name`" class="inline-flex items-center px-2 h-full hover:bg-purple-200">Search
        Meals</router-link>
      <router-link :to="`/by-letter`" class="inline-flex items-center px-2 h-full hover:bg-purple-200">Meals By
        Letter</router-link>
      <router-link :to="`/by-ingredient`" class="inline-flex items-center px-2 h-full hover:bg-purple-200">Meals By
        Ingredients</router-link>
    </div>
  </header>
</template>

<script lang='ts' setup>

</script>

<style lang="scss" scoped></style>