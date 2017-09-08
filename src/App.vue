<template lang="pug">
  #app.columns.is-gapless
    sidebar
    main-content
</template>

<script>
  import Sidebar from './components/Sidebar';
  import MainContent from './components/MainContent';

  export default {
    name: 'app',
    components: {
      Sidebar,
      MainContent
    }
  };
</script>

<style lang="scss">
  @import './assets/stylesheets/main.scss';

  #app {
    font-family: 'Mplus 1p';
    height: 100%;
    margin-bottom: 0;
  }
</style>
