<template>
  <div class="relative" @mouseover="hover=true" @mouseleave="hover=false">
    <img src="../assets/card1.jpg" alt="cards" class="rounded-lg" />
    <div v-if="hover" class="top-0 bg-dark opacity-50 inset-0 w-full h-full absolute rounded-lg"></div>
    <div class="flex flex-col justify-between">
      <div class="flex justify-end">
        <button
          class="bg-red-600 text-white font-semibold rounded-full px-4 py-3 absolute top-4 right-3"
        >
          Save
        </button>
      </div>
      <div class="flex items-center w-full">
        <div
          class="flex-grow absolute bottom-3 left-5 opacity-75 hover:opacity-100"
        >
          <div class="bg-light text-dark px-2 rounded-full">
            <span class="material-icons font-semibold text-dark text-base pr-2">/ </span
            >twitter.com
          </div>
        </div>
        <button
          type="button"
          name="button"
          class="absolute bottom-3 right-10 ml-auto mr-3 text-dark bg-light rounded-full w-8 h-8 flex items-center justify-center text-sm opacity-75 hover:opacity-100"
        >
          <span class="material-icons font-bold text-base">ios_share</span>
        </button>
        <button
          type="button"
          name="button"
          class="bg-light absolute bottom-3 right-3 text-dark rounded-full w-8 h-8 flex items-center justify-center opacity-75 hover:opacity-100"
        >
          <span class="material-icons font-bold text-base">more_horiz</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["src"],
  data(){
    return{
      hover:false
    }
  }
};
</script>

<style></style>
