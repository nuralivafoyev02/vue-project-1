<template>
  <div id="app">
    <Header />
    <Intro />
  </div>
</template>
<script setup>
import Header from './components/header.vue';
import Intro from './components/intro.vue';
</script>

<style lang="scss" scoped>
#app {  
  background: url('@/assets/background-img.png') no-repeat center center;
  background-size: cover;
  background-position: center;
  min-height: 100vh;
}
</style>