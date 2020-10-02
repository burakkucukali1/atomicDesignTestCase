<template><div>
 <div class="timeline">
    <h3 style="margin-bottom:3px">| HAFTALAR</h3>
    <card v-for="(item, index) in weekList" :key="index" :weekNum="item"/>
  </div>
</div>
</template>

<script>
import card from '../molecules/card'
export default {
    name:"timeline",
    components: {
        card
    },
      data(){
    return {
      weekList:Array.from({length: 52}, (_, i) => i + 1),
    }
  },
}
</script>

<style>
.timeline{
   width: 500px;
   height: 520px;
   background-color: #eee; 
   border-radius: 5px;
   padding: 20px;
   overflow:scroll;
   font-family: Arial, Helvetica, sans-serif;
}
</style>