<script setup>
const route = useRoute()
const slug = computed(() => route.params.slug)
const { data } = await useFetch(`https://api.nuxtjs.dev/mountains/${slug.value}`)
</script>
<template>{{ data }}</template>