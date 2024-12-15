<script setup>
import CardTemplate from '@/components/cards_UI/cards/cards_00_theFools.vue'
import CardTemplate2 from '@/components/cards_UI/cards/cards_01_theMagician.vue'
import CardTemplate3 from '@/components/cards_UI/cards/cards_02_theEmpress.vue'
import '@/assets/cards/cards_style.css'

</script>

<template>

  <div class="background">
      <CardTemplate />
      <CardTemplate2 />
      <CardTemplate3 />
  </div>
</template>

<style scoped>
  .background {
    position: relative;
    float: right;
    min-width: 10000px;
    text-align: left;
  }

</style>
<script>


export default {
  name: 'CardShuffle',
  data() {
    return {
      currentData: ["asdad"]
    }
  },
  created () {
    const CardSeq = [];
    for(let i=0; i<54; i++){
      let num = Math.floor(Math.random() * 54) + 1;
      for(const j in CardSeq){
        while(num === CardSeq[j]){
          num = Math.floor(Math.random() * 54) + 1;
        }
      }
      CardSeq.push(num);
    }
    console.log(CardSeq);
  }
}

</script>