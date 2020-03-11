<template>
  <div id="app">
    <buttonView></buttonView>
  </div>
</template>

<script>
import buttonView from './components/moButton/View'
export default {
  name: "App",
  components: {
    buttonView
  }
};
</script>

<style lang="scss">
@import "./styles/common";
</style>
