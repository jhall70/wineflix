<template>
    <section class="primary-navigation">
      <h1>WineFlix</h1>
      <ul class="navigation-links">
        <li v-for="link in links" :key="link.linkLabel" :class="{active: link.isActive}">
          <a :href="link.linkHref">{{ link.linkLabel }}</a>
        </li>
      </ul>
    </section>
</template>

<script>
export default {
  name: 'PrimaryNavigation',
  props: {
    links: Object,
  },
};
</script>
