<template>
  <section>
    <div
      class="container mx-auto flex md:px-24 md:py-10 md:flex-row flex-col items-center"
    >
      <div
        class="lg:flex-grow mt-5 md:mt-0 md:w-1.5/2 lg:pr-24 md:pr-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 pl-3 items-center text-center"
      >
        <h1 class="text-7xl text-greenPrimary sm:text-left my-4 text-left">
          Good Food Us Good Mood
        </h1>
        <p class="text-xl text-[#757575] my-4 font-extralight text-left">
          I would think that conserving our natural resources should be a
          conservative position: Not to waste food, and not to throw away a lot
          of the food that we buy.
        </p>
        <div class="flex justify-center py-4">
          <a
            href="#"
            class="inline-flex text-white bg-greenPrimary py-2 px-6 rounded-full text-lg shadow-xl"
          >
            Daftar Sekarang
          </a>
          <a
            href="#"
            class="ml-4 inline-flex text-[#333333] bg-grayButton py-2 px-6 focus:outline-none rounded-full text-lg"
          >
            About Us
          </a>
        </div>
      </div>
      <img alt="hero" src="~/assets/img/hero.png" class="w-full h-auto" />
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style scoped>
.container::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('~/assets/img/background.png') center/cover no-repeat;
  opacity: 0.02;
  z-index: -1;
}
</style>
