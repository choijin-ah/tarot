<script setup>
  import CardTemplate from './components/cards/CardTemplete.vue'


</script>

<template>
  <div class="background">
    <div id="app">
      <CardTemplate />
    </div>
    </div>
</template>

<style scoped>
  .background {
    margin: 0;
    background: url('src/assets/landing_logo.jpg') repeat ;
    top:0;
    left: 0;
    width: 100%;
    height: 100%;
    position: fixed;
    padding:0;
  }

</style>
