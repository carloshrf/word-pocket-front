<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  }
}
</script>

<style>

body {
  margin: 0;
  max-width: 1350px;
  margin: 0 auto;
}

h1, h2, h3, 
h4, h5, h6, 
span, p, ul, 
li, button, a {
  padding: 0;
  margin: 0;
}

a {
  text-decoration: none;
  color: inherit;
}

input, textarea {
  font-family: Poppins;
}

* {
  box-sizing: border-box;
}

:root {
  font-family: Poppins;
  --bg-color: #f6f5f5;
  --main-color: #f37121;
  --button-color: #111d5e;
  --secondary-color: #ffbd69;
}
</style>
