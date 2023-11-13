<template>
  <section class="py-16 mb-6">
    <div class="container mx-auto">
      <!-- Title and Subtitle -->
      <div class="text-left mb-8 pl-3">
        <h2 class="text-4xl font-extrabold text-textBlack mb-2">
          Browse Our Trending
        </h2>
        <h3 class="text-greenPrimary text-2xl">Receipt</h3>
      </div>

      <!-- Trending Cards -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12">
        <!-- Render Trending Cards -->
        <div
          v-for="trending in trendingWithRemainingStars"
          :key="trending.name"
          :class="
            trending.color +
            ' p-8 rounded-xl shadow-lg w-80 h-80 mx-auto sm:mx-0 trending-card relative'
          "
        >
          <div class="relative z-10">
            <!-- Image -->
            <img
              :src="trending.image"
              :alt="trending.name"
              class="w-auto h-32 object-cover mb-4 rounded"
            />

            <!-- Content -->
            <h3 class="text-2xl font-bold mb-2">{{ trending.name }}</h3>
            <p class="text-greenPrimary mb-2 text-lg">{{ trending.type }}</p>
            <div class="flex items-center mb-2">
              <!-- Render Star Ratings -->
              <span
                v-for="star in trending.rating"
                :key="`${trending.name}-${star}`"
                class="text-[#f78414] text-xl"
              >
                ★
              </span>
              <span
                v-for="star in trending.remainingStars"
                :key="`${trending.name}-remaining-${star}`"
                class="text-[#c9c9c9] text-xl"
              >
                ★
              </span>
            </div>
          </div>

          <!-- Pattern Image -->
          <div
            class="absolute inset-0 bg-cover bg-center opacity-80 z-0 trending-pattern"
          ></div>
        </div>
      </div>

      <!-- Show All Button -->
      <div class="hidden lg:flex justify-center mt-10">
        <button
          href="#"
          class="inline-flex text-white bg-greenPrimary py-3 px-7 rounded-full text-lg shadow-xl"
        >
          All Receipt
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      trendings: [
        {
          name: 'Pizza Paperoni',
          type: 'Pizza',
          rating: 4,
          image: require('~/assets/img/trending/1.png'),
          color: 'bg-skySecondary',
        },
        {
          name: 'Pizza Meat',
          type: 'Pizza',
          rating: 3,
          image: require('~/assets/img/trending/2.png'),
          color: 'bg-skySecondary',
        },
        {
          name: 'Donar Kebab',
          type: 'Kebab',
          rating: 5,
          image: require('~/assets/img/trending/3.png'),
          color: 'bg-blueSecondary',
        },
        {
          name: 'Salmon Roll',
          type: 'Salmon',
          rating: 4,
          image: require('~/assets/img/trending/4.png'),
          color: 'bg-redSecondary',
        },
        {
          name: 'Cupcake Choco',
          type: 'Cupcake',
          rating: 4,
          image: require('~/assets/img/trending/5.png'),
          color: 'bg-greenSecondary',
        },
        {
          name: 'Doughnut Milk',
          type: 'Doughnut',
          rating: 5,
          image: require('~/assets/img/trending/6.png'),
          color: 'bg-leafSecondary',
        },
        {
          name: 'Doughnut Unicorn',
          type: 'Doughnut',
          rating: 4,
          image: require('~/assets/img/trending/7.png'),
          color: 'bg-leafSecondary',
        },
        {
          name: 'Kathi Kebab',
          type: 'Kebab',
          rating: 4,
          image: require('~/assets/img/trending/8.png'),
          color: 'bg-blueSecondary',
        },
      ],
    }
  },
  computed: {
    trendingWithRemainingStars() {
      return this.trendings.map((trending) => ({
        ...trending,
        remainingStars: 5 - trending.rating,
      }))
    },
  },
}
</script>

<style scoped>
.trending-card {
  position: relative;
  overflow: hidden;
}

.trending-card:hover::before {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url('~/assets/img/pattern.png');
  background-size: cover;
  background-position: center;
  opacity: 0.05;
}
</style>
