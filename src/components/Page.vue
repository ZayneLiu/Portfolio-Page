<template>
  <div :id="'page-'+pageNo" class="fullpage">
    <slot></slot>
  </div>
</template>

<style>
</style>

<script lang='ts'>
export default {
  name: "Page",
  props: {
    pageNo: Number,
  },
};
</script>