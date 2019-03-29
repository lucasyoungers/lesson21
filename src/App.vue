<template>
  <div id="app">
    <img alt="Active Martial Arts Logo" src="./assets/active-logo.png">
    <ul class="AwardsList">
      <award-card v-for="award in awards" v-bind:key="award.id" v-bind:award="award"/>
    </ul>
  </div>
</template>

<script>
import AwardCard from "./components/AwardCard.vue";

export default {
  name: "app",
  components: {
    AwardCard
  },
  data() {
    return {
      awards: [
        {
          id: 1,
          title: "High Kick",
          detail: "Kick over your head 10 times in under 10 seconds.",
          imageurl: require("./assets/high-kick.jpg")
        },
        {
          id: 2,
          title: "Closed Fist",
          detail: "Break a 1 inch wood board with closed fist.",
          imageurl: require("./assets/closed-fist.jpg")
        },
        {
          id: 3,
          title: "Dragon Spirit",
          detail: "Complete Your Form 100 Times",
          imageurl: require("./assets/dragon-spirit.jpg")
        }
      ]
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  background: linear-gradient(rgba(200, 200, 200, 0.6), rgba(80, 80, 80, 0.7));
}
</style>