<script>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Footer
  }
}

</script>

<template>
  <div id="app">
    <Navbar />
    <main>
      <router-view />
    </main>
    <Footer />
    </div>
</template>

<style>
#app {
  min-height: 100vh;
    display: flex;
  flex-direction: column;
  }

main {
  flex: 1;
  padding: 2rem;
}
</style>
