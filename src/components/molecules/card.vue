<template>
  <div class="card">
    <icon 
     :weekNum= "weekNum"/>
    <cardContent 
     :weekNum= "weekNum" />
  </div>
</template>

<script>
import icon from "../atoms/icon";
import cardContent from "../atoms/cardContent";
export default {
  name: "card",
  props: ["weekNum"],
  components: {
    icon,
    cardContent,
  },
};
</script>

<style>
.card {
  display: flex;
  align-items: center;
  background-color: #fff;
  box-shadow: 0 3px 5px rgba(black, 0.4);
  border-bottom: 1px solid #c4c4c4;
  padding: 3.3px;
}
</style>