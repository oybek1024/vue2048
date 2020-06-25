<template>
  <div id="app">
    <p class="title">Vue 2048 Game</p>
    <MainContent/>
  </div>
</template>

<script>
import MainContent from './components/MainContent'
export default {
  components: {
    MainContent
  },
  data() {
    return {
      
    };
  },
  methods: {
    
  }  
};
</script>

<style lang="scss">
#app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    width: 100vw;
    height: 100vh;
    display: grid;
    grid-template-rows: auto 1fr auto;

    .title {
        padding: 15px;
        text-align: center;
        font-size: 1.5rem;
    }
}
</style>
