<script setup>
import CardTemplate from '@/components/cards_UI/cards/CardTemplate.vue'
import CardTemplate2 from '@/components/cards_UI/cards/CardTemplate2.vue'
import CardTemplate3 from '@/components/cards_UI/cards/CardTemplate3.vue'


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