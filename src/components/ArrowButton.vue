<template>
  <button
    class="btn"
    @click="onClick"
  >
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
  props: { arrowType: String, onClick: Function }
};
</script>

<style src="../assets/styles/ArrowButton.css" scoped/>



