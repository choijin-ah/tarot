

<template>
    <span class="wrapper">
      <span id="cards_00_theFools" class="card" :class="{'reverse': currentData === cardR}" >
       </span>
      <span class="card_outer"></span>
    </span>
</template>

<style scoped>

</style>

<script>

export default {
  name: 'CardTemplate',
  data() {
    return {
      cardF: ['카드이름', '정방향', '뜻'],
      cardR: ['카드이름', '역방향', '뜻'],
      currentData: [],
      index:[],
    }
  },
  created () {
      this.currentData = Math.random() < 0.5 ? this.cardF : this.cardR;
      console.log(this.currentData);
      return {

      }
  },
}
</script>