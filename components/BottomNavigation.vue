<template>
  <div
    class="fixed bottom-0 left-0 right-0 bg-white border-t border-gray-300 p-1 z-10"
  >
    <div class="flex justify-around items-center text-[#757575]">
      <button
        @click="navigate('home')"
        class="flex flex-col items-center justify-center"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-6 h-6 mb-1"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
          />
        </svg>
        Home
      </button>

      <button
        @click="navigate('promotion')"
        class="flex flex-col items-center justify-center"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-6 h-6 mb-1"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
          />
        </svg>
        Promotion
      </button>

      <button
        @click="navigate('other')"
        class="flex flex-col items-center justify-center"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-6 h-6 mb-1"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
          />
        </svg>
        Other
      </button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    navigate(route) {
      console.log(`Navigating to ${route}`)
    },
  },
}
</script>

<style scoped></style>
