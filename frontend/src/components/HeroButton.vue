<template>
<button :class="buttonClass">
  <FontAwesomeIcon :icon="iconName" />
  <span>{{ buttonLabel }}</span>
</button>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

export default {
  name: 'HeroButton',
  components: {
    FontAwesomeIcon,
  },
  props: {
    iconName: String,
    buttonLabel: String,
    buttonClass: String,
  },
};
</script>
