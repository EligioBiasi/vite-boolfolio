<script>
  import AppMain from './components/AppMain.vue';
  import AppHeader from './components/AppHeader.vue';
  import AppFooter from './components/AppFooter.vue';

  export default{
    name: 'App',
    components:{
      AppMain,  
      AppHeader,  
      AppFooter,  
    }
  }
</script>

<template>
  <header>
    <AppHeader />
  </header>
  <main>
    <AppMain />
  </main>
  <footer>
    <AppFooter />
  </footer>
</template>

<style lang="scss">
@use './styles/partials/general.scss' as *;

.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
