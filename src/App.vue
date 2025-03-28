<template>
  <div id="app">
    <Header />
    <router-view/>
    <HelloWorld />
    <Sobrecomponent />
    <Costumerfoto />

    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import HelloWorld from './components/HelloWorld.vue';
import Sobrecomponent from './components/sobre.vue';
import Costumerfoto from './components/foto.vue';

export default {
  name: 'App',
  components: {
    Header,
    HelloWorld,
    Sobrecomponent,
    Costumerfoto,
    Footer
  }
};
</script>