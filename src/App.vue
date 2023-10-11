<script setup>
import UserDetails from './components/UserDetails.vue';

console.log(UserDetails)
</script>

<template>
<h1 class="text-center">This is app vue component</h1>
  <section class="user-details">
    <UserDetails/>

  </section>
</template>

<style scoped>
  .user-details{
    width: 90%;
    margin: 0 auto;
  }
</style>
