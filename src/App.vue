<template>
  <div id="ppp">
    <header class="header">
      <div class="header-content">
        <img class="header-content__logo" src="./assets/img/tinder.svg" alt="Logo Tinder">
        <h1 class="header-content__title">meet a 'borg</h1>
        <h2 class="header-content__title2">Ça va pécho chez les robots 🤖🍆🍑</h2>
      </div>
    </header>
    <main class="main" id="app">
      <RobotFilter/>
      <!-- ici on lie robots à la liste Robots pour le passer ensuite dans les props des enfants -->
      <RobotList :robots="Robots"/> 
    </main>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import RobotList from "./components/RobotList.vue";
import FilterButtons from "./components/FilterButtons.vue";
import RobotFilter from "./components/RobotFilter.vue";
import axios from "axios";

export default {
  name: "ppp",
  data() {
    return {
      Robots: [],
      FilteredRobots:[]
    };
  },

  created() {
    axios
      .get(
        "https://wt-902485dbb4fca4fccee3a0efcde5b34c-0.sandbox.auth0-extend.com/robots"
      )
      .then(response => {
        this.Robots = response.data;
      });
  },
  components: {
    //  HelloWorld
    RobotList,
    RobotFilter
  }
};
</script>

<style lang="css">
@import "./assets/css/style.min.css";

#ppp {
  height: 100%;
}
</style>