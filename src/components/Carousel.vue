<template>
  <div>
    <div class="card-carousel">
      <Card
        class="current-element"
        :headline="currentElement.headline"
        :text="currentElement.text"
        :imgName="currentElement.imgName"
      />
    </div>
  </div>
</template>
<script>
import Card from "./Card.vue";

export default {
  name: "Carousel",
  props: { cards: Array },
  components: { Card },

  data() {
    return {
      currentElementIndex: 0
    };
  },
  computed: {
    currentElement() {
      return this.cards[this.currentElementIndex];
    }
  }
};
</script>

<style src="../assets/styles/Carousel.css" scoped/>