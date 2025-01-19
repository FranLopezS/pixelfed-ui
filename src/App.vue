<script setup>
import BodyFeed from './components/BodyFeed.vue';
import HeaderFeed from './components/HeaderFeed.vue';
</script>

<template>
  <div class="container">
    <HeaderFeed />
    <BodyFeed />
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  row-gap: 50px;
  width: 1000px;
  align-items: center;
  background-color: rgb(252, 252, 243);
  padding-top: 10px;
  padding-bottom: 10px;
  border-radius: 5px;
}

@media (width < 1000px) {
  .container {
    width: 100%;
  }
}

</style>