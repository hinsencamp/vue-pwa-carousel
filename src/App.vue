<template>
  <div id="app">
    <header>
      <img
        src="./assets/logo.png"
        alt="Vue.js PWA"
      >
      <span>Progressive Vue App</span>
    </header>
    <main>
      <h1 v-html="headline" />
      <div class="section">
        <h2>{{this.sections[0].headline}}</h2>
        <Carousel :cards="cards" />
      </div>
      <div class="section">
        <h2>{{this.sections[0].headline}}</h2>
        <Carousel :cards="cards" />
      </div>
      <div class="section">
        <h2>{{this.sections[0].headline}}</h2>
        <Carousel :cards="cards" />
      </div>
      <div class="section">
        <h2>{{this.sections[1].headline}}</h2>
        <p>{{this.sections[1].text}}</p>
      </div>
      <Imprint />
    </main>
  </div>
</template>

<script>
import Imprint from "./components/Imprint";
import Carousel from "./components/Carousel";
export default {
  name: "app",
  components: { Imprint, Carousel },

  data() {
    return {
      headline:
        'Learn Everything about building Progressive Vue Apps with <a href="https://medium.com/@Fa_Hinse">@Fa_Hinse</a> on Medium!',
      sections: [
        { headline: "What can Service Workers do?" },
        {
          headline: "How do Service Workers exactly work?",
          text:
            "Read more about Service Workers it in my other tutorials. There we implement and discuss the astonishing offline-first experience that Service Workers provide."
        }
      ],

      cards: [
        {
          headline: "Make App available Offline",
          text: "All static files get pre-cached by using the Caching API.",
          imgName: "setting.svg"
        },
        {
          headline: "Use background sync to defer actions",
          text:
            "Data can be entered offline, it's sent when online again thanks to the Background Sync API.",
          imgName: "cloud.svg"
        },
        {
          headline: "Send Push Notifications",
          text:
            "The Notifications API lets us send push notifications to re-engage users.",
          imgName: "antenna.svg"
        }
      ]
    };
  }
};
</script>

<style src="./assets/styles/App.css"/>


