<template>
  <header class="hero">
    <img class="hero-image" src="/wine-hero.webp">
    <nav class="navigation">
      <PrimaryNavigation :links="getPrimaryLinks"/>
      <SecondaryNavigation label="S"/>
    </nav>
    <HeroContent
        :heroTitle="getHeroTitle"
        :heroImageUrl="getHeroImageUrl"
        :heroSubTitle="getHeroSubTitle"
        :heroDescription="getHeroDescription"/>
  </header>
  <main>
    <CategorySection sectionTitle="Drink Again" :sectionValues="getDrinkAgainItems"/>
    <CategorySection sectionTitle="Keep Drinking" :sectionValues="getKeepDrinkingItems"/>
  </main>
</template>

<script>
import PrimaryNavigation from '@/components/PrimaryNavigation.vue';
import SecondaryNavigation from '@/components/SecondaryNavigation.vue';
import HeroContent from '@/components/HeroContent.vue';
import CategorySection from '@/components/CategorySection.vue';

export default {
  name: 'App',
  components: {
    PrimaryNavigation,
    SecondaryNavigation,
    HeroContent,
    CategorySection,
  },
  data() {
    return {
      primaryLinks: [
        {
          isActive: true,
          linkHref: '#',
          linkLabel: 'Home',
        },
        {
          isActive: false,
          linkHref: '#',
          linkLabel: 'Whites',
        },
        {
          isActive: false,
          linkHref: '#',
          linkLabel: 'Reds',
        },
        {
          isActive: false,
          linkHref: '#',
          linkLabel: 'Blends',
        },
      ],
      heroContent: {
        title: 'Rex Goliath',
        subtitle: 'His Royal Majesty is back.',
        imageUrl: '/rex-goliath-logo.png',
        description: 'America\'s most unhinged rooster is out of retirement, and this time? He\'s mad as hell.  Experience the unapologetic flavor burst of Rex Goliath.',
      },
      wines: [
        {
          id: 1,
          imageUrl: '/red-wine.jpg',
          isNew: true,
          label: 'Wine',
          isFinished: true,
        }, {
          id: 2,
          imageUrl: '/red-wine.jpg',
          label: 'Wine',
          isFinished: true,
        }, {
          id: 3,
          imageUrl: '/red-wine.jpg',
          label: 'Wine',
          isNew: true,
          isFinished: true,
        }, {
          id: 4,
          imageUrl: '/red-wine.jpg',
          label: 'Wine',
          isFinished: true,
        }, {
          id: 5,
          imageUrl: '/red-wine.jpg',
          label: 'Wine',
          isNew: true,
          isFinished: true,
        }, {
          id: 6,
          imageUrl: '/red-wine.jpg',
          label: 'Wine',
          isFinished: true,
        }, {
          id: 7,
          imageUrl: '/red-wine.jpg',
          label: 'Wine',
          isFinished: true,
        }, {
          id: 8,
          imageUrl: '/red-wine.jpg',
          label: 'Wine',
          isFinished: true,
        }, {
          id: 1,
          imageUrl: '/red-wine.jpg',
          progress: 8,
          label: 'Wine',
        }, {
          id: 2,
          imageUrl: '/red-wine.jpg',
          progress: 66,
          label: 'Wine',
        }, {
          id: 3,
          imageUrl: '/red-wine.jpg',
          progress: 98,
          label: 'Wine',
        }, {
          id: 4,
          imageUrl: '/red-wine.jpg',
          progress: 44,
          label: 'Wine',
        }, {
          id: 5,
          imageUrl: '/red-wine.jpg',
          progress: 70,
          label: 'Wine',
        }, {
          id: 6,
          imageUrl: '/red-wine.jpg',
          progress: 15,
          label: 'Wine',
        }, {
          id: 7,
          imageUrl: '/red-wine.jpg',
          progress: 22,
          label: 'Wine',
        }, {
          id: 8,
          imageUrl: '/red-wine.jpg',
          progress: 32,
          label: 'Wine',
        }],
    };
  },
  computed: {
    getKeepDrinkingItems() {
      return this.wines.filter((item) => !item.isFinished);
    },
    getDrinkAgainItems() {
      return this.wines.filter((item) => item.isFinished === true);
    },
    getPrimaryLinks() {
      return this.primaryLinks;
    },
    getHeroTitle() {
      return this.heroContent.title;
    },
    getHeroSubTitle() {
      return this.heroContent.subtitle;
    },
    getHeroImageUrl() {
      return this.heroContent.imageUrl;
    },
    getHeroDescription() {
      return this.heroContent.description;
    },
  },
};
</script>

<style lang="scss">
</style>
