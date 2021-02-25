<template>
  <button 
    class="default-btn"
  >
    <slot />
  </button>
</template>

<script>
export default {
  name: 'Button',
}
</script>

<style scoped>
  .default-btn {
    background-color: var(--button-color);
    color: white;
    border: none;
    border-radius: 15px;
    padding: 20px 60px;
    font-size: 28px;
    cursor: pointer;
    outline: none;
    width: 300px;

    transition: background-color .2s;
  }

  .default-btn:hover {
    background-color: black;
  }
</style>