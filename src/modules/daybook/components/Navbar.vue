<template>
  <!--Navbar goes here-->
  <nav class="bg-primary">
    <div class="px-8 mx-auto">
      <div class="flex justify-between text-white">
        <div class="flex space-x-4">
          <!--Logo-->
          <div>
            <a class="flex items-center py-5 px-2 text-gray-700 hover:text-gray-300">
              <img
                src="../../../assets/logo.png"
                alt="logo"
                width="24"
                class="mx-2"
              >
              <span class="font-bold text-white">Daybook</span>
            </a>
          </div>
          <!--primary nav-->
          <!--<div class="hidden md:flex items-center space-x-1">
            <button class="py-5 px-3 hover:text-gray-300">Home</button>
            <button class="py-5 px-3 hover:text-gray-300">Features</button>
            <button class="py-5 px-3 hover:text-gray-300">Pricing</button>
          </div>-->
        </div>

        <!--secondary nav-->
        <div class="hidden md:flex items-center space-x-1 mr-5">
          <!--<button class="py-5 px-3">Login</button>-->
          <button class="py-2 px-3 bg-yellow-400 text-yellow-900 rounded transition duration-300 hover:bg-yellow-300 hover:text-yellow-800">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 16l4-4m0 0l-4-4m4 4H7m6 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h4a3 3 0 013 3v1" />
            </svg>
          </button>
        </div>

        <!--mobile button goes here-->
        <div class="md:hidden flex items-center">
          <button @click="showHidden">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
          </button>
        </div>

      </div>
    </div>

    <!-- mobile menu -->
    <div :class="hidden">
      <a class=" py-2 px-4 text-sm hover:bg-gray-200 block">Home</a>
      <a class="block py-2 px-4 mr-full text-sm hover:bg-gray-200">Feature</a>
      <a class="block py-2 px-4 text-sm hover:bg-gray-200">Precing</a>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  data(){
    return {
      hidden: 'hidden'
    }
  },
  methods: {
    showHidden(){
      this.hidden == 'hidden'? this.hidden = '' : this.hidden = 'hidden'
    }
  }
}
</script>

<style scoped>

</style>