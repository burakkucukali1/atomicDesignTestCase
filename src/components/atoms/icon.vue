<template>
  <div :style="classDeciderSvg" class="svg">
    <div></div>
    <div>
      <p>{{ weekNum }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "icon",
    props: ["weekNum"],
    data() {
    return {
      activeWeek: 5,
    };
  },
  computed: {
    classDeciderSvg() {
      if (this.activeWeek == this.weekNum) {
        return "background-color:green";
      } else if (this.activeWeek < this.weekNum) {
        return "background-color:#c4c4c4";
      }
    },
  },
};
</script>
<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.svg {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 1.5em;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: #000;
  color: #ddd;
  text-align: center;
}
</style>