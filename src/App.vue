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
      <h1>{{ headline }}</h1>
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
        <span>
          Read this <a
            href='http://creativecommons.org/licenses/by/3.0/'
            title='Learn about Service Workers'
          >other</a> article of mine!
        </span>
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
        "Here You Learn Everything about building Progressive Vue Apps!",
      sections: [
        { headline: "What does a Service Worker do?" },
        {
          headline: "How does a Service Worker exactly work?"
        }
      ],

      cards: [
        {
          headline: "Makes App available Offline",
          text:
            "By using the CachingAPI all static elements on an app can be pre-cached",
          imgName: "setting.svg"
        },
        {
          headline: "Use background sync to defer actions",
          text:
            "User inputs entered when offline are sent in the background once they get connectivity.",
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


