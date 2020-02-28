<template>
  <div id="main">
    <Home v-if="!isLoading"/>
    <Loading v-if="isLoading" class="loading"/>
  </div>
</template>

<script>
import Home from './views/home'
import Loading from './components/loading'
export default {
  data(){
    return {
      isLoading: true
    }
  },
  created(){
    setTimeout(() => {
      this.isLoading = false;
    }, 2000);
  },
  name: 'App',
  components: {
    Home,
    Loading
  }
}
</script>

<style lang="scss">
#main{
  height: 100%;
  width: 100%;
  background-color: #F0ECE3;
  .loading{
    width: 100%;
    height: 100%;
    background-color: #333;
    position: absolute;
    top: 0;
    left: 0;
  }
}
</style>
