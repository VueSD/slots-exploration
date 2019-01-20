<template>
  <div>
    <slot :currentTime="currentTime">
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
