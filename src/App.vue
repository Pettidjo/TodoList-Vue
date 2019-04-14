<template>
  <div id="app">
    <Header />
    <router-view/>
  </div>
</template>

<script>
import Header from './components/Header.vue';

export default {
  name: "aspp",
  components: {
    Header
  }
}
</script>


<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  } 

  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }

  .btn {
    display: inline-block;
    border: none;
    background: #555;
    padding: 7px 20px;
    color: #FFF;
    cursor: pointer;
  }

  .btn:hover {
    background: #666;
  }
</style>
