<template>
  <div class="navbar">
    <img src="../assets/images/Rick_and_Morty.svg.png" alt="Logo" id="logo" />

    <section class="functions">
      <router-link to="/" class="nav-link">Personagens</router-link>
      <router-link to="/about" class="nav-link">Sobre mim</router-link>
    </section>
  </div>
</template>

<style scoped>
#logo {
  height: 40px;
  margin-left: 40px;
}

.navbar {
  align-items: center;
  background: #587c53;
  display: flex;
  justify-content: space-between;
  padding-left: 2rem;
  padding-right: 2rem;
  position: fixed;
  z-index: 2;
  width: 100%;
}

.nav-link:hover {
  color: rgb(20, 208, 255);
}

.functions {
  width: 250px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  color: aliceblue;
  font-family: "Montserrat", sans-serif;
  font-weight: 600;
  overflow-x: hidden;
  margin-right: 40px;
}
</style>
