<template>
  <div id="app">
  <Navbar />
  <Jumbotron/>
  <Overview/>
  <Features/>
  <Tech/>
  <Page/>
  <Contact/>      
  </div>
</template>

<script>

// Import the styles directly. (Or you could add them via script tags.)


export default {}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.icon{
  font-size: 100px;
}
.sansserif {
  font-family: sans-serif;
  font-size: 28px;
  font-weight: bold;
}
</style>
