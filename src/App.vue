<template>
  <div class="container">
    <main>
      <Header v-model="searchWord" />
      <Definition :searchWord='searchWord'/>
    </main>
  </div>
</template>

<script setup>
import Header from './components/Header.vue';
import Definition from './components/Definition.vue';
import { ref, watch } from 'vue';

const searchWord = ref();

</script>

<style lang="scss" scoped>
div.container {
  height: 100vh;
  overflow: hidden;
  background-color: #282c34;

  main {
    max-width: 1000px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    color: white;
    padding: 1rem;
  }
}
</style>
