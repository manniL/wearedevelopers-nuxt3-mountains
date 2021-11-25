<script setup>
const { data: mountains } = await useFetch(`https://api.nuxtjs.dev/mountains`)
</script>
<template>
  <ul>
    <li v-for="mountain in mountains">
      <NuxtLink :to="'/mountains/' + mountain.slug">{{ mountain.title }}</NuxtLink>
    </li>
  </ul>
</template>