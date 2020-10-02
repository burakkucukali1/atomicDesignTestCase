<template>
  <div>
    <div :style="classDeciderContent" class="cardContent">
      <p>{{ weekNum }}. HAFTA 2020</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "cardContent",
  props: ["weekNum"],
   data() {
    return {
      activeWeek: 5,
    };
  },
  computed: {
    classDeciderContent() {
      return this.activeWeek < this.weekNum ? "color:#c4c4c4" : "";
    },
  },
};
</script>

<style>
.cardContent {
  flex-grow: 1;
  margin-left: 20px;
  margin-right: 20px;
}
</style>