<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>
<script>
import '@/assets/css/tailwind.css'

export default {
  
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');

h1 {
  font-family: 'Roboto', sans-serif;
  letter-spacing: 0.5px;

}

h2 {
  font-family: 'Roboto', sans-serif;

}
</style>
