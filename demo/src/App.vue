<template>
  <div id="app">
    <img src="./assets/logo.png">
  <br>
  <div>
    Links <a v-show="mostrar" @click="mostrar=false" href="#/"> Home </a>  <a v-show="!mostrar" href="#/about" @click="mostrar=true"> About </a> 
  </div>
  <!--  <HelloWorld/> -->
  <main>
    <router-view />
  </main>
    <Hello/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Hello from './components/Hello'
import Home from './components/Home'
import About from './components/About'
//import router from './router/myrouter';
import Vue from 'vue';
import VueRouter from 'vue-router';

Vue.use(VueRouter);

const router = new VueRouter({
    routes: [
      { path: '/', component: Home },
      { path: '/about', component: About }
    ]
  });


export default {
  name: 'App',
  components: {
    HelloWorld,
    Hello
  },
  router,
  data() {
  return { ruta : location.pathname, mostrar : false}
  },
  computed: {
    path(){ this.ruta =  location.pathname}
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
