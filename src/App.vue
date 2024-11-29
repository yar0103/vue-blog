<template>
  <nav class="navbar navbar-expand-lg bg-body-tertiary">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarTogglerDemo02" aria-controls="navbarTogglerDemo02" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Link</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Link2</a>
        </li>
      </ul>
    </div>
  </div>
</nav>

<router-link to="/">메인</router-link>
<router-link to="/list">list</router-link>
<router-link to="/detail">detail</router-link>


<div class="mt-4">
  <router-view :blogData="blogData"></router-view>
</div>

<!-- <List :blogData="blogData"/> -->

</template>

<script >
// import List from './components/List.vue';
import blogData from './assets/blogData.js';

export default {
  name: 'App',
  data(){
    return{
      blogData: blogData
    }
  },
  // components: {
  //   List: List,
  // }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
