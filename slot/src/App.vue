<template>
  <div id="app">
    <!-- <HelloWorld>
      qqqqqerwerwerwer
      <div slot="left">我是具名插槽left</div>
      <div slot="right">我是具名插槽1</div>qqqqqerwerwerwer
    </HelloWorld>-->
    <!--
        #default  ===  v-slot:default
        {user:myName}  ===  将user属性重命名为myName

     -->
    <ScopeSlot :user="user">
      <template #default="{ parentProp = { firstName: 'Guest' } }">
        {{ parentProp.firstName }}
      </template>
    </ScopeSlot>
  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue'
  import ScopeSlot from './components/ScopeSlot.vue'

  export default {
    name: 'app',
    data() {
      return {
        user: {
          firstName: "郭",
          lastName: "奕",
        }
      }
    },
    components: {
      HelloWorld, ScopeSlot
    }
  }
</script>

<style>
  #app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
