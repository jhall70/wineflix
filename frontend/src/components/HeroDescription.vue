<template>
  <p>
    {{ description }}
  </p>
</template>

<script>

export default {
  name: 'HeroDescription',
  props: {
    description: String,
  },
};
</script>
