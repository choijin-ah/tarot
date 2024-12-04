

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
  name: 'CardWand1',     // 1. 컴포넌트의 이름을 지정해요
  props: {},
  data() {
    return {
      CardName: "1번 카드"
    }
  },
}
</script>