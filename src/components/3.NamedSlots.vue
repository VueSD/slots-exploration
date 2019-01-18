<template>
  <div>
    <h3>Component content</h3>

    <slot></slot>

    <slot name="footer"></slot>
  </div>
</template>

<script>
export default {
  mounted() {
    // console.log(this.$slots);
  }
};
</script>
