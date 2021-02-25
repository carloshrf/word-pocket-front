<template>
  <router-link to="/" class="container">
    <div class="goback-icon" />
    <span>go back</span>
  </router-link>
</template>

<script>
export default {
  name: 'GoBack'
}
</script>

<style scoped>
.container {
  display: inline-flex;
  justify-items: center;
  align-items: center;

  cursor: pointer;
}

.goback-icon {
  width: 15px;
  height: 15px;
  border-left: 3px solid #c70039;
  border-bottom: 3px solid #c70039;
  transform: rotate(45deg);
}

span {
  color: #c70039;
}
</style>