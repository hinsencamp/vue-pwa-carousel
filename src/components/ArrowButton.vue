<template>
  <button
    class="btn"
    :class="this.styles"
  >
    <img
      class="icon"
      :src="require(`@/assets/svg/${arrowType}.svg`)"
      :alt="arrowType + 'arrow'"
    >
  </button>
</template>

<script>
export default {
  name: "ArrowButton",
  props: { arrowType: String },

  data() {
    return {
      props: this.$props
    };
  },
  computed: {
    styles() {
      const styles = {
        left: "prev-btn",
        right: "next-btn"
      };
      return styles[this.arrowType];
    }
  }
};
</script>

<style src="../assets/styles/ArrowButton.css" scoped/>



