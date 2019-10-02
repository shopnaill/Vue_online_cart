<template>
  <div id="app">
    <app-header />
    <router-view />
  </div>
</template>

<script>
import AppHeader from "@/components/AppHeader.vue";
export default {
  name: "app",
  components: {
    AppHeader
  }
};
</script>
<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  padding: 19px;
  margin: 0px;
  -webkit-box-shadow: 1px 1px 3px #dbdbe0;
  box-shadow: 1px 1px 3px #dbdbe0;
  margin-top: -8px;
  margin-left: -7px;
  margin-right: -7px;
  padding-left: 110px;
  padding-right: 110px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
