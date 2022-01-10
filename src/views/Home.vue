<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <h1 class="text-4xl font-bold underline">
      Hello world!
    </h1>

    <button @click="goToDaybook" class="hover:bg-green-700 mt-1 px-3 py-2 bg-primary mx-2 rounded-md text-white">Primary</button>
    <button @click="goToDaybook" class="hover:bg-green-700 mt-1 px-3 py-2 bg-secondary mx-2 rounded-md text-white">Secondary</button>
    <button @click="goToDaybook" class="hover:bg-green-700 mt-1 px-3 py-2 bg-success mx-2 rounded-md text-white">Success</button>
  </div>
</template>

<script>
  export default {
    methods: {
      goToDaybook(){
        this.$router.push({name: 'no-entry'})
      }
    }
  }
</script>