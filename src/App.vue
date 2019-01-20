<template>
  <div id="app">
    <NoSlots></NoSlots>
    <hr>
    <BasicSlots></BasicSlots>
    <hr>
    <NamedSlots></NamedSlots>
    <hr>
    <ScopedSlots>
      <template slot-scope="{ currentTime }">
        <h1>Time Formats:</h1>
        <p>{{ new Date(currentTime) }}</p>
        <p>{{ new Date(currentTime).toDateString() }}</p>
        <p>{{ new Date(currentTime).toLocaleString() }}</p>
        <p>{{ new Date(currentTime).toLocaleTimeString() }}</p>
        <p>{{ new Date(currentTime).toString() }}</p>
        <p>{{ new Date(currentTime).toTimeString() }}</p>
      </template>
    </ScopedSlots>
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
