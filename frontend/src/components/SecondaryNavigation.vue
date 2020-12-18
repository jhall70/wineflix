<template>
    <section class="secondary-navigation">
        <span class="user-avatar">
          <a href="#">{{ label }}</a>
        </span>
    </section>
</template>

<script>
export default {
  name: 'SecondaryNavigation',
  props: {
    label: String,
  },
};
</script>
