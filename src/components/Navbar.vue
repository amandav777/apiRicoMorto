<template>
  <div class="navbar">
    
    <router-link to="/">home</router-link>
    <router-link to="/about">About</router-link>
    <router-view></router-view>
  </div>
</template>

<style scoped>
.navbar {
  background-color: rgb(0, 0, 0);
  width: 100%;
  flex-direction: row;
}
</style>
