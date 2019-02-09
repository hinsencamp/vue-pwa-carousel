<template>
  <div class=carousel-container>
    <div class="card-carousel">
      <Card
        class="current-element"
        headline="A fantastic Headline"
        infoText="Here you can write some more fantastic details"
        imgName="antenna.svg"
      />
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
      //
    };
  }
};
</script>
