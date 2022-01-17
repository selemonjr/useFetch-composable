<template>
<div id="app">
  <div>
     <Fetch/>
  </div>
</div>
</template>

<script>
import Fetch from './components/Fetch.vue';
export default {
  name: 'App',
  components: {
    Fetch
  }
}
</script>

<style>
* {
  margin:0;
  padding:0;
  box-sizing:border-box;
}
body {
  height:100vh;
  width:100%;
  font-family:sans-serif;
  padding:1rem;
}
</style>
