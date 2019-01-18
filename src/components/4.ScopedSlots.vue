<template>
  <div>
    <h3>Component content:</h3>

    <slot :currentTime="currentTime">
      <!-- <p>The current time is: {{ currentTime }}</p> -->
    </slot>
  </div>
</template>

<script>
export default {
  data: () => ({
    currentTime: null
  }),
  mounted() {
    const updateTime = () => {
      this.currentTime = Date.now();
      setTimeout(updateTime, 1000);
    };
    updateTime();
  }
};
</script>
