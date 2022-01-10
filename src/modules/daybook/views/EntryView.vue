<template>
  <div class="entry-title flex justify-between p-2">

    <div>
      <span class="text-success text-2xl font-bold">15</span>
      <span class="mx-1 text-2xl">Julio</span>
      <span class="mx-2 text-3xl font-light">2021, jueves</span>
    </div>

    <div class="flex">
      <button class="bg-red-500 p-2 flex rounded-md mx-2 text-white font-bold hover:bg-red-700 mt-2">
        Borrar
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16" />
        </svg>
      </button>
      <button class="bg-primary p-2 flex rounded-md text-white font-bold hover:bg-green-700 mt-2">
        subir foto
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-8l-4-4m0 0L8 8m4-4v12" />
        </svg>
      </button>
    </div>
  </div>

  <hr>
  <div class="flex flex-col px-3">
    <textarea
      class="mt-3"
      placeholder="¿Qué sucedió hoy?"
    ></textarea>
  </div>

  <img src="https://www.xtrafondos.com/descargar.php?id=3183&resolucion=2560x1440" alt="entry-picture">

  <Fab icon="M8 7H5a2 2 0 00-2 2v9a2 2 0 002 2h14a2 2 0 002-2V9a2 2 0 00-2-2h-3m-1 4l-3 3m0 0l-3-3m3 3V4"></Fab>

</template>

<script>
import {defineAsyncComponent} from 'vue'


export default {
  name: "EntryView",
  components:{
    Fab: defineAsyncComponent(() => import('../components/Fab.vue'))
  }
}
</script>

<style lang="scss" scoped>

textarea{
  font-size: 20px;
  border: none;
  height: 100% !important;

  &:focus {
    outline: none;
  }
}

img{
  width: 200px;
  position: fixed;
  bottom: 150px;
  right: 20px;
  box-shadow: 0px 5px 10px rgba($color: #000000, $alpha: 0.5);
}

</style>