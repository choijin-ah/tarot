
<template>
  <div @click="show = !show" class="landing-page">
    <div  class="start-button">
      Press Any Button
    </div>
  </div>
</template>

<style scoped>
.landing-page {
  width: 100%;
  height: 100%;
  text-align: center;
  position: fixed;
  filter: blur(5px);
}
</style>
<script setup>
export default {
  name: 'start_button',
  click() {
    this.currentData = Math.random() < 0.5 ? this.cardF : this.cardR;
    console.log(this.currentData);
    return {

    }
  },
  methods:{
    click(){
      this.result = this.input
    }
  }
}
</script>
