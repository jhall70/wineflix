<template>
  <img :alt="title" :src="imageUrl">
</template>

<script>

export default {
  name: 'HeroImage',
  props: {
    title: String,
    imageUrl: String,
  },
};
</script>
