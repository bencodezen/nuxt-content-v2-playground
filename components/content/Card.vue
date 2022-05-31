<script setup>
const props = defineProps({
  type: {
    type: String
  },
  hidden: {
    type: Boolean,
    default: false
  }
})
</script>

<template>
  <div style="background-color: yellow">
    <h1><slot name="title" /></h1>
    <h2>{{ type }} - {{ hidden }}</h2>
    <slot />
  </div>
</template>
