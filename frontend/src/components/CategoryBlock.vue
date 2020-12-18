<template>
<div class="wine">
  <img :src="imgSrc" alt="Wine">
  <span v-if="showNew" class="new-badge">New!</span>
  <div v-if="showProgress" class="amount-consumed">
    <progress min="0" max="100" :value="progressValue"></progress>
  </div>
</div>
</template>

<script>
export default {
  name: 'CategoryBlock',
  props: {
    item: Object,
  },
  computed: {
    showProgress() {
      return typeof this.item.progress !== 'undefined';
    },
    progressValue() {
      return this.item.progress;
    },
    showNew() {
      return typeof this.item.isNew !== 'undefined' && this.item.isNew;
    },
    imgSrc() {
      return this.item.imageUrl;
    },
  },
};
</script>
