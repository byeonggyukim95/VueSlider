<template>
  <div id="app">
    <app-header />
    <div id="content" class="content">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import header from './components/layout/header.vue';

export default {
  name: 'App',
  components: {
    'app-header' : header
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.title {
  padding: 100px;
}

.slider {
  width: 100%;
  height: 150px;
  position: absolute;
  left: 10%;
  top: 20%;  
  overflow: hidden;
}
.slider-item{
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 60%;
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  gap: 3px;
}
</style>
