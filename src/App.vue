<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
  body{
    background: #eee;
    margin: 20px;
    font-family: tahoma;
  }
#app {
  width: 80%;
  margin: 0 auto;
  background: #fff;
  border-top: 3px solid #EA1E63;
  padding: 10px;
  border-radius: 2px;
  box-shadow: 1px 3px 5px rgba(0,0,0,0.2);
  color: #333;
}
</style>
