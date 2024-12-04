

<template>
  <div id="CardNum" class="card"></div>
</template>

<style scoped>
  #CardNum{
    height: 200px;
    width: 150px;
    background-color: black;
  }


</style>

<script>

export default {
  name: 'RandomData',
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
  computed: {

  },
}
</script>