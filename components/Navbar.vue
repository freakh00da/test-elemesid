<template>
  <nav class="bg-white p-4">
    <div class="container mx-auto flex items-center justify-between">
      <div>
        <img src="../assets/logo/elemes.svg" alt="Logo" class="w-52 h-auto" />
      </div>

      <div class="hidden sm:flex flex-grow justify-center items-end">
        <a href="#" class="text-neutral-500 mx-2 text-lg">Home</a>
        <a href="#" class="text-neutral-500 mx-2 text-lg">About</a>
        <a href="#" class="text-neutral-500 mx-2 flex flex-col items-end">
          <span class="bg-red-500 text-white text-xs px-2 py-1 rounded-3xl"
            >HOT</span
          >
          <span class="mr-3 text-lg">Promotions</span>
        </a>
        <a href="#" class="text-neutral-500 mx-2 text-lg">Blogs</a>
        <a href="#" class="text-neutral-500 mx-2 text-lg">Contact Us</a>
      </div>

      <div class="flex items-center space-x-2 sm:space-x-4">
        <a href="#" class="text-gray-800 hidden sm:inline">Masuk</a>

        <a href="#" class="bg-greenPrimary text-white px-4 py-2 rounded-full"
          >Daftar Sekarang</a
        >
      </div>
    </div>
  </nav>
</template>

<script>
export default {}
</script>
