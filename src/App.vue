<template>
  <div id="app">
    <Header />
    <router-view/>
    <HelloWorld />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    Header,
    HelloWorld,
    Footer
  }
}
</script>
