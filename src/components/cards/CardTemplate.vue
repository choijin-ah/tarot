

<template>
  <div id="CardNum" class="card" :class="{'reverse': currentData === cardR}" >
    곰
   </div>
</template>

<style scoped>
  #CardNum{
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
  name: 'CardTemplate',
  data() {
    return {
      cardF: ['카드이름', '정방향', '뜻'],
      cardR: ['카드이름', '역방향', '뜻'],
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