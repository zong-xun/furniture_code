<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Navbar></Navbar>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';
import Navbar from '../components/Navbar.vue';
export default {
  name: 'Home',
  components: {
    HelloWorld,
    Navbar
  }
};
</script>
