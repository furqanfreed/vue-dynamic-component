<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    
    <keep-alive>
      <component v-bind:is="component" />
    </keep-alive>

    <button v-on:click="toggle">Toggle</button>
  </div>
</template>

<script>

import Component1 from './components/Component1.vue'
import Component2 from './components/Component2.vue'

export default {
  name: 'app',
  components: {
    Component1,
     Component2
  },
  data (){
    return {
      component:"Component2"
    }
  },
  methods: {
    toggle(){
      if (this.component === Component1) {
        this.component = Component2;
      } else {
        this.component = Component1;
      }
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
