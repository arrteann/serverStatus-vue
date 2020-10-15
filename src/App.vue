<template>
  <div id="app">
    <app-header></app-header>
    <div>
      <app-server> </app-server>
      <app-server> </app-server>
      <app-server> </app-server>
      <app-server> </app-server>
    </div>

    <app-footer></app-footer>
  </div>
</template>

<script>
import AppHeader from "./components/shared/Header";
import AppFooter from "./components/shared/Footer";
import AppServer from "./components/servers/ServersStatus";
export default {
  name: "App",
  components: {
    AppHeader,
    AppFooter,
    AppServer,
  },
};
</script>

<style lang="scss">
#app {
  display: grid;
  grid-template-rows: 100px 1fr 60px;
  grid-template-areas:
    "header"
    "content"
    "footer";
  height: 70vh;
  overflow: hidden;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  padding: 30px 20px;
  border-radius: 5px;
  box-shadow: 0 3px 6px rgba($color: #000000, $alpha: 0.1);
}
</style>
