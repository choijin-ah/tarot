

<template>
  <div id="CardNum" class="card">
    <div class="test">
      테스트
    </div>
  </div>
</template>

<style scoped>
  #CardNum{
    height: 200px;
    width: 150px;
    background-color: #123456;
  }


</style>

<script>

export default {
  name: 'RandomCard',
  data() {
    return {
      cardF: ['카드이름', '정방향', '뜻'],
      cardR: ['카드이름', '역방향', '뜻'],
      currentData: []
    }
  },
  methods: {
    generateRandom() {
      this.currentData = Math.random() < 0.5 ? this.cardF : this.cardR
    }
  },
  created() {
    this.generateRandom();
    console.log(this.currentData);
  }
}
</script>