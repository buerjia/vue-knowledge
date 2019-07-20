<template>
  <div class="hello">
    <slot></slot>
    <slot name="left"></slot>
    HelloWorld<br>
    <slot name="right"></slot>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<style scoped>

</style>
