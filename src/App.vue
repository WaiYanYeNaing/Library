<template>
  <div id="app">
    <Navbar />
    <router-view />
    <Footer />
  </div>
</template>

<script>
import Footer from './components/Footer.vue'
import Navbar from './components/Navbar.vue'
export default {
  name: 'App',
  components: {
    Navbar,
    Footer,
  },

  data: () => ({
    //
  }),
}
</script>

<style>
body {
  background-color: rgb(255, 251, 226);
}
#app {
  position: relative;
}
</style>
