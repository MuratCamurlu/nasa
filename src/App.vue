<template>
  <div>
    <WelcomePlanet v-if="showWelcomeScreen" />
  </div>
</template>

<script>
import WelcomePlanet from "./components/WelcomePlanet.vue";
export default {
  name: "App",
  data() {
    return {
      showWelcomeScreen: true,
    };
  },
  created() {
    setTimeout(() => {
      this.showWelcomeScreen = false;
    }, 5000);
  },
  components: { WelcomePlanet },
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  background-color: #0b3d91;
  color: black;
  overflow: hidden;
}
</style>
