<template>
  <section class="py-16">
    <div class="container mx-auto">
      <!-- Title and Subtitle -->
      <div class="text-left mb-2 pl-3">
        <h2 class="text-4xl font-extrabold text-textBlack mb-2">
          Browse our Category
        </h2>
        <h3 class="text-greenPrimary text-2xl">Receipt</h3>
      </div>

      <!-- Category Cards -->
      <div
        class="relative flex mb-6 items-end pb-2 justify-between overflow-hidden h-64"
        ref="categoryContainer"
      >
        <div class="flex space-x-4">
          <!-- Render Category Cards -->
          <div
            v-for="category in categories"
            :key="category.name"
            :class="
              category.color +
              ' pt-10 rounded shadow-md w-72 h-52 transform transition-transform hover:scale-105 category-card'
            "
          >
            <!-- Image -->
            <img
              :src="category.image"
              :alt="category.name"
              class="w-auto h-14 mx-auto object-cover mb-5 rounded transition-transform transform hover:scale-105"
            />

            <!-- Content -->
            <h3 class="text-base font-bold mb-1 text-center">
              {{ category.name }}
            </h3>
            <p class="text-gray-600 text-sm text-center">
              {{ category.total }}
            </p>
          </div>
        </div>
      </div>

      <!-- Prev and Next Buttons with Icons -->
      <div class="flex justify-end space-x-2">
        <button
          class="bg-greenPrimary text-white py-2 px-4 rounded-full focus:outline-none flex items-center"
          @click="scrollCategory('prev')"
        >
          <img
            src="~/assets/icons/prev.svg"
            alt="Previous"
            class="w-6 h-auto mr-2"
          />
          PREV
        </button>
        <button
          class="bg-greenPrimary text-white py-2 px-4 rounded-full focus:outline-none flex items-center"
          @click="scrollCategory('next')"
        >
          NEXT
          <img
            src="~/assets/icons/next.svg"
            alt="Next"
            class="w-6 h-auto ml-2"
          />
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    scrollCategory(direction) {
      const container = this.$refs.categoryContainer
      const scrollAmount = direction === 'next' ? 600 : -600
      container.scrollBy({
        top: 0,
        left: scrollAmount,
        behavior: 'smooth',
      })
    },
  },
  props: {
    subtitle: {
      type: String,
      required: true,
    },
    categories: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style scoped>
.category-card {
  position: relative;
  overflow: hidden;
}

.category-card:hover::before {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url('~/assets/img/pattern.png');
  background-size: cover;
  background-position: center;
  opacity: 0.05;
  transition: opacity 0.3s ease;
}
</style>
