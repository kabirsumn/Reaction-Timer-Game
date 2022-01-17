<template>
  <h1>Catch The Ball as soon as you can</h1>
  <button class="btn">Start</button>
  <Circle />
</template>

<script>
import Circle from './components/Circle.vue';
export default {
  name: 'App',
  components: { Circle },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
