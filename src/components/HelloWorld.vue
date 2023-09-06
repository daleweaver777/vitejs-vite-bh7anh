<script setup>
defineProps({
  name: String,
  phone: String,
  cell: String,
});
</script>

<template>
  <p>Name: {{ name }}</p>
  <p>Phone: {{ phone }}</p>
  <p>Cell: {{ cell }}</p>
</template>
