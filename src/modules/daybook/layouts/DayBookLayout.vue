<template>
  <Navbar/>

  <div class="flex grid gird-cols-12 grid-flow-col">
    <div class="entryList"><EntryList/></div>
    <div class="col-span-11 routerView">
      <router-view/>
    </div>
  </div>
</template>

<script>
import { defineAsyncComponent } from 'vue'

export default {
  name: "DayBookLayout",
  components: {
    Navbar: defineAsyncComponent(() => import('../components/Navbar.vue')),
    EntryList: defineAsyncComponent(() => import('../components/EntryList.vue'))
  }
}
</script>

<style scoped>

.entryList {
  width: 350px;
}

.routerView {
  width: 1550px;
}

</style>