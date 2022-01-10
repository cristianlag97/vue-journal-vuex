<template>
  <button class="bg-primary hover:bg-green-700">
    <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10 text-white mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" :d="icon" />
    </svg>
  </button>
</template>

<script>
export default {
  name: "Fab",
  props:{
    icon: {
      type: String,
      default: 'M12 6v6m0 0v6m0-6h6m-6 0H6'
    }
  }
}
</script>

<style lang="scss" scoped>

button {
  position: fixed;
  bottom: 20px;
  right: 20px;
  width: 65px;
  height: 65px;
  border-radius: 100%;
}

</style>