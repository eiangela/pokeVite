<script setup>
import { ref } from 'vue';

let num = ref(0)

</script>

<template>
<!--navbar-->
<nav class="navbar navbar-expand-lg navbar-dark bg-primary">
  <div class="container-fluid">
  <router-link class="navbar-brand" to="/">
      <img src="https://raw.githubusercontent.com/yurimarcon/pokevite-preparacao/d0d020c76b0aa306f54033bd7325e1fe130287e7/src/assets/icon.svg" alt="Logo" width="30" height="24" class="d-inline-block align-text-top">
      PokeVite
  </router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <router-link class="nav-link" aria-current="page" to="/">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/about">About</router-link>
        </li>
      </ul>
    </div>
  </div>
</nav>

<!--content-->
<div class="main">
  <router-view></router-view>
</div>

<footer class="bg-primary text-light">
<div> Desing in
  {{ new Date().getFullYear() }}
</div>
</footer>
</template>

<style>
body {
  height: 100vh;
  background: rgb(31,247,245);
  background: linear-gradient(163deg, rgba(31,247,245,1) 2%, rgba(42,6,247,0.7176120448179272) 100%);
}

footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 56px;
}
</style>