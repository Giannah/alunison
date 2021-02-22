<template>
  <Header />
  <div id="content">
    <main role="main" aria-labelledby="main-title">
      <FirstView />
      <About />
    </main>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import FirstView from '@/components/FirstView.vue'
import About from '@/components/About.vue'

export default {
  name: 'App',
  components: {
    Header,
    FirstView,
    About,
  },
}
</script>

<style lang="scss">
html {
  box-sizing: border-box;
  margin: 0 auto;
}
h1,
h2,
h3,
h4,
h5,
h6 {
  font-weight: bold;
}
section {
  margin: 2rem;
}
h1 {
  color: #025f5f;
  font-size: 2.5rem;
}
.section-title {
  color: #ffbb00;
  text-align: left;
}
.section-subtitle {
  color: #00bbbb;
  font-size: 2rem;
  margin-bottom: 2rem;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#content {
  margin-top: 6rem;
}
</style>
