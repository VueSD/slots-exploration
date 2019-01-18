<template>
  <div id="app">

    <NoSlots></NoSlots>

    <hr>

    <BasicSlots></BasicSlots>

    <hr>

    <NamedSlots></NamedSlots>

    <hr>

    <ScopedSlots></ScopedSlots>

  </div>
</template>

<script>
import NoSlots from "./components/1.NoSlots";
import BasicSlots from "./components/2.BasicSlots";
import NamedSlots from "./components/3.NamedSlots";
import ScopedSlots from "./components/4.ScopedSlots";

export default {
  components: {
    NoSlots,
    BasicSlots,
    NamedSlots,
    ScopedSlots
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
