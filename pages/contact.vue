<script setup>
const { data } = await useAsyncData('contactContent', () => {
  return queryContent('/contact').findOne()
})

const { data: SocialData } = await useAsyncData('socialContent', () => {
  return queryContent('/platforms').findOne()
})
</script>

<template>
  <h1>Contact Page</h1>
  <ContentRenderer :value="data" />
  <pre>{{ SocialData }}</pre>
  <!-- <ul>
    <li v-for="social in SocialData.body">
      {{ social }}
    </li>
  </ul> -->
  <button>Hi</button>
</template>

<style></style>
