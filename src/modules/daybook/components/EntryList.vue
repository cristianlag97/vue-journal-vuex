<template>
  <div class="entry-list-container">
    <div class="px-2 pt-2">
      <input
        type="text"
        class="mt-1 block w-full px-3 py-2 bg-white border border-gray-300 rounded-md text-sm shadow-sm
          placeholder-gray-400 focus:outline-none focus:border-blue-400 focus:ring-1 focus:ring-sky-500
          disabled:bg-gray-50 disabled:text-gray-500 disabled:border-gray-200 disabled:shadow-none
          invalid:border-pink-500 invalid:text-pink-600
          focus:invalid:border-pink-500 focus:invalid:ring-pink-500"
        placeholder="Buscar entrada"
      >
    </div>
    <div class="entry-scrollarea">
      <Entry v-for="item in 100" :key="item"/>
    </div>
  </div>
</template>

<script>
import { defineAsyncComponent } from 'vue'


export default {
  name: "EntryList",
  components: {
    Entry: defineAsyncComponent(() => import('../components/Entry'))
  }
}
</script>

<style lang="scss" scoped>

input {
  width: 300px;
}

.entry-list-container{
  width: 350px;
  border-right: 1px solid #2c3e50;
  height: calc(100vh - 10px);
}

.entry-scrollarea{
  height: calc(100vh - 60px);
  overflow: scroll;
}


</style>