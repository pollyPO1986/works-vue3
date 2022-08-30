<template>
  <img alt="Vue logo" src="./assets/logo.png">
  {{ message }}
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import { ref, onMounted } from 'vue'
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  setup () {
    let message = ref('Hello')

    onMounted(() => {
      message = 'Hi'
    })

    return {
      message
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
