<template>
  <div>
    <hero-section />
    <category-section :subtitle="subtitle" :categories="categories" />
    <trending-section />
    <div v-if="isMobileScreen">
      <bottom-navigation />
    </div>
    <div v-else>
      <footer-section />
    </div>
  </div>
</template>

<script>
import HeroSection from '~/components/HeroSection.vue'
import CategorySection from '~/components/CategorySection.vue'
import TrendingSection from '~/components/TrendingSection.vue'
import BottomNavigation from '~/components/BottomNavigation.vue'
import FooterSection from '~/components/FooterSection.vue'

export default {
  components: {
    HeroSection,
    CategorySection,
    TrendingSection,
    BottomNavigation,
    FooterSection,
  },
  layout: 'navbar',
  data() {
    return {
      subtitle: 'Receipt',
      categories: [
        {
          name: 'Cake',
          total: '22 items',
          image: require('~/assets/img/cake.png'),
          color: 'bg-greenSecondary',
        },
        {
          name: 'Pizza',
          total: '25 items',
          image: require('~/assets/img/pizza.png'),
          color: 'bg-skySecondary',
        },
        {
          name: 'Kebab',
          total: '12 items',
          image: require('~/assets/img/kebab.png'),
          color: 'bg-blueSecondary',
        },
        {
          name: 'Salmon',
          total: '22 items',
          image: require('~/assets/img/salmon.png'),
          color: 'bg-redSecondary',
        },
        {
          name: 'Doughnut',
          total: '11 items',
          image: require('~/assets/img/doughnut.png'),
          color: 'bg-leafSecondary',
        },
        {
          name: 'Cake 2',
          total: '22 items',
          image: require('~/assets/img/cake.png'),
          color: 'bg-greenSecondary',
        },
        {
          name: 'Pizza 2',
          total: '25 items',
          image: require('~/assets/img/pizza.png'),
          color: 'bg-skySecondary',
        },
        {
          name: 'Kebab 2',
          total: '12 items',
          image: require('~/assets/img/kebab.png'),
          color: 'bg-blueSecondary',
        },
        {
          name: 'Salmon 2',
          total: '22 items',
          image: require('~/assets/img/salmon.png'),
          color: 'bg-redSecondary',
        },
        {
          name: 'Doughnut 2',
          total: '11 items',
          image: require('~/assets/img/doughnut.png'),
          color: 'bg-leafSecondary',
        },
      ],
      isMobileScreen: false,
    }
  },
  mounted() {
    window.addEventListener('resize', this.handleResize)
    this.handleResize()
  },
  destroyed() {
    window.removeEventListener('resize', this.handleResize)
  },
  methods: {
    handleResize() {
      const mobileWidth = 768
      this.isMobileScreen = window.innerWidth <= mobileWidth
    },
  },
}
// tambahan disini test kedua
</script>

<style scoped></style>
