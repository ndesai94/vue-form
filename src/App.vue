<template>
  <div id="app">
    <Layout :my-title="message"/>
  </div>
</template>

<script>
import Layout from './components/Layout'

export default {
  name: 'App',
  data () {
    return {
      message: "Welcome to the Vue Form Table!"
    }
  },
  components: {
    Layout
  }
}
</script>

<style>
</style>
