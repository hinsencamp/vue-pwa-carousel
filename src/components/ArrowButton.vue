<template>
  <button class="btn">
    <img
      class="icon"
      :src="require(`@/assets/svg/${arrowType}.svg`)"
      :alt="arrowType + ' arrow'"
    >
  </button>
</template>
<script>
export default {
  name: "ArrowButton",
  props: { arrowType: String }
};
</script>

<style src="../assets/styles/ArrowButton.css" scoped/>



