<template>
  <div id="app" class="app">
    <app-sidenav></app-sidenav>
    <main class="app-main">
      <app-navbar></app-navbar>
      <router-view/>
      <app-footer></app-footer>
    </main>
  </div>
</template>

<script>
import AppSidenav from './components/AppSidenav'
import AppNavbar from './components/AppNavbar'
import AppFooter from './components/AppFooter'

export default {
  name: 'App',
  components: {
    AppSidenav,
    AppNavbar,
    AppFooter
  }
}
</script>

<style lang="scss">
@import './assets/scss/index.scss';

.app {
  display: grid;
  grid-template-columns: 270px auto;
  height: 100vh;

  .app-main {
    display: grid;
    grid-template-rows: 70px auto 30px;
  }
}
</style>
