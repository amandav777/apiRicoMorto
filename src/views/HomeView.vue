<script setup>
import Card from '../components/Card.vue';
import Navbar from '@/components/Navbar.vue';

</script>

<template>
  <div class="container">
    <Navbar />
    <Card/>
  </div>
</template>


<style>
.container{
  display: flex;
  flex-direction: column;

}

</style>