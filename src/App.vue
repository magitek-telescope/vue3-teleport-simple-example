<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" />
    <hello-world />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import HelloWorld from './components/HelloWorld.vue'

export default defineComponent({
  name: 'App',
  components: {
    HelloWorld
  }
})
</script>
