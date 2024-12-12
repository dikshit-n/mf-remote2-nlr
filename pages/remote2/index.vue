<template>
  <h1>Remote 2</h1>
</template>

<script setup lang="ts">
const { $moduleConfig } = useNuxtApp();
console.log($moduleConfig, 'config from remote 2')
definePageMeta({
  layout: 'base'
})
</script>