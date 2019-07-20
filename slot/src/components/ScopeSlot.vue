<template>
  <div>
    <span>
      <slot :user="user">{{ user.lastName }}</slot>
      {{ user.lastName }}
    </span>
  </div>
</template>

<script>
  export default {
    name: "ScopeSlot",
    props:{
      user:{
        type:Object
      }
    }
  }
</script>

<style scoped>
</style>