<template>
  <section class="category">
    <h2>{{ sectionTitle }}</h2>
    <ul>
      <li v-for="item in sectionValues" :key="item.id">
        <CategoryBlock :item="item" />
      </li>
    </ul>
  </section>
</template>

<script>
import CategoryBlock from '@/components/CategoryBlock.vue';

export default {
  name: 'CategorySection',
  props: {
    sectionTitle: String,
    sectionValues: Object,
  },
  components: {
    CategoryBlock,
  },
};
</script>
