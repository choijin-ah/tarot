

<template>
  <span id="CardNum" class="card" :class="{'reverse': currentData === cardR}" >
    2
  </span>
</template>

<style scoped>
  #CardNum{
    display: inline-block;
    height: 200px;
    width: 150px;
    background: linear-gradient(45deg, Violet, Orange);
    font-size: 38px;
  }
  .reverse{
    transform: scaleY(-1) scaleX(-1);

  }
</style>

<script>

export default {
  name: 'CardTemplate2',
  data() {
    return {
      cardF: ['카드이름2', '정방향', '뜻'],
      cardR: ['카드이름2', '역방향', '뜻'],
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