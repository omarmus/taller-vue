<template>
  <div id="app" class="app">
    <app-sidenav></app-sidenav>
    <main class="app-main">
      <app-navbar></app-navbar>
      <div class="main">
        <router-view/>
      </div>
      <app-footer></app-footer>
    </main>
  </div>
</template>

<script>
import AppSidenav from './components/layout/AppSidenav'
import AppNavbar from './components/layout/AppNavbar'
import AppFooter from './components/layout/AppFooter'

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

  .main {
    padding: 20px 30px;
  }
}
</style>
