<template>
  <div id="app">
    <header>
      <img src="./assets/icon_analytics.svg" alt="icon" />
    </header>
    <div class="body">
      <CardComponent
        :headline="headlineWeeklyStats"
        :content="contentWeeklyStats"
      />
    </div>
    <footer>© Alexander Ehrling</footer>
  </div>
</template>

<script>
import { ref } from "vue";
import CardComponent from "./components/CardComponent.vue";

export default {
  components: {
    CardComponent,
  },
  name: "App",
  setup() {
    const headlineWeeklyStats = ref("Weekly Stats");
    const contentWeeklyStats = ref("Content");

    return {
      headlineWeeklyStats,
      contentWeeklyStats,
    };
  },
};
</script>

<style>
body {
  margin: 0;
  background-color: #0f0f0f;
  color: #ffffff;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#app {
  display: flex;
  flex-direction: column;
  min-height: 50vh;
  text-align: center;
}

header {
  display: flex;
  align-items: start;
  justify-content: start;
  padding: 0.5rem;
}

.body {
  display: flex;
  align-items: start;
  justify-content: center;
  padding: 0.5rem;
  height: 100vh;
}

footer {
  display: flex;
  align-items: start;
  justify-content: start;
  padding: 0.5rem;
  color: #858585;
  font-size: 0.8em;
}
</style>
