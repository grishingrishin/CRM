<template>
  <div id="app">
    <Layout>
      <Users/>
    </Layout>
  </div>
</template>

<script>
import Layout from './components/Layout.vue';
import Users from './components/Users/';

export default {
  name: 'App',
  components: {
    Layout,
    Users,
  }
}
</script>

<style>
#app {
  font-weight: 300;
  font-family: 'Roboto', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
