<template>
  <div>{{ (test, number) }}</div>
</template>

<script setup lang="ts">
defineProps<{ test: string; number: number }>();
</script>

<style scoped></style>
