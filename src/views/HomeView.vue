<template>
    <div class="px-20 w-full h-full flex-wrap py-3">
      <div class="w-1/5">

        <Card  class="w-full h-full"/>
      </div>
  </div>
</template>

<script>
import Card from '@/components/Card.vue';

  export default {
    name: 'Home',

    components: {
    Card
},
  }
</script>
