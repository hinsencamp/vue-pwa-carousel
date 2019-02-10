<template>
  <div class="card">
    <img
      class="card-icon"
      :src="require(`@/assets/svg/${imgName}`)"
      alt="card icon"
    />
    <div class='card-content'>
      <h3 class='headline'>{{headline}}</h3>
      <p>{{text}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    headline: String,
    imgName: String,
    text: String
  }
};
</script>

<style src="../assets/styles/Card.css" scoped>