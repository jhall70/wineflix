<template>
  <div class="hero-content">
    <h2>
      <HeroImage :title="heroTitle" :imageUrl="heroImageUrl"/>
    </h2>
    <HeroSubTitle :subTitle="heroSubTitle" />
    <HeroDescription :description="heroDescription" />
    <ul class="controls">
      <li>
        <HeroButton
            iconName="play"
            buttonLabel="Drink"
            buttonClass="primary-action"/>
      </li>
      <li>
        <HeroButton
            iconName="info-circle"
            buttonLabel="More Info"
            buttonClass="secondary-action"/>
      </li>
    </ul>
  </div>
</template>

<script>
import HeroButton from '@/components/HeroButton.vue';
import HeroImage from '@/components/HeroImage.vue';
import HeroSubTitle from '@/components/HeroSubTitle.vue';
import HeroDescription from '@/components/HeroDescription.vue';

export default {
  name: 'HeroContent',
  components: {
    HeroButton,
    HeroImage,
    HeroSubTitle,
    HeroDescription,
  },
  props: {
    heroTitle: String,
    heroSubTitle: String,
    heroImageUrl: String,
    heroDescription: String,
  },
};
</script>
