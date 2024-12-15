

<template>
  <span class="wrapper">
  <span id="cards_02_theEmpress" class="card" :class="{'reverse': currentData === cardR}" >
  </span>
    <span class="card_outer"></span>
    </span>
</template>

<style scoped>

</style>

<script>

export default {
  name: 'CardTemplate3',
  data() {
    return {
      cardF: ['카드이름3', '정방향', '뜻'],
      cardR: ['카드이름3', '역방향', '뜻'],
      currentData: []
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