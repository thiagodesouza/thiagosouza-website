<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>

export default {
  name: 'App',
};
</script>

<style lang="scss">
/**
 * Imports
 */
@import "./styles/default.scss";
@import "./styles/icons.scss";

#app {
  display: flex;
  align-items: stretch;
  justify-content: center;
  min-height: 100vh;
}
</style>
