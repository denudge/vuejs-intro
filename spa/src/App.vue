<template>
  <div id="app">

    <nav class="navbar navbar-default">
      <div class="container-fluid">
        <div class="navbar-header">
          <a class="navbar-brand" href="#">Single Page Application</a>
        </div>
        <ul class="nav navbar-nav">
          <li class="active"><router-link to="/">Home</router-link></li>
          <li><router-link to="/activities">Activities</router-link></li>
        </ul>
      </div>
    </nav>

    <router-view/>
  </div>
</template>

<script>

var $ = require('jquery')
window.$ = window.jQuery = $
require('bootstrap-sass')

export default {
  name: 'app'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
