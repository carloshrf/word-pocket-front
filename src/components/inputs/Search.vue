<template>
  <div class="container">
    <img src="../../assets/icons/loupe.svg" alt="loupe">
    <!-- Icons made by <a href="https://www.flaticon.com/authors/pixel-perfect" -->
    <input type="text" placeholder="search...">
  </div>  
</template>

<script>
export default {
  name: 'Search'
}
</script>

<style scoped>
  .container {
    height: 50px;
    display: flex;
    align-items: center;
    padding-right: 10px;
    box-shadow: 1px 5px 14px 2px rgba(0,0,0,0.2)
  }

  .container img {
    height: 60%;
    padding: 0 15px;
  }

  .container input {
    height: 100%;
    width: 100%;
    border: none; 
    font-size: 20px;
    outline: none;
  }
</style>