<script setup lang='ts'>
import { computed, onMounted, ref } from 'vue';
import store from '../store';
import axiosClient from '../axiosClient.js'

const meals = computed(() => store.state.meals)
const letters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'.split("")
const ingredients = ref([])

onMounted(async () => {
  const res = await axiosClient.get('/list.php?i=list')
  ingredients.value = res.data
})


</script>

<template>
  <div class="flex flex-col p-8">
    <input type="text" class="rounded border-2 border-gray-200 w-full" placeholder="Search for Meals">

    <div class="flex justify-center gap-2 mt-2">
      <router-link :to="`/letter/${letter}`" v-for='letter of letters' :key='letter'>
        {{ letter }}
      </router-link>
    </div>
    
  </div>
</template>

<style scoped></style> 