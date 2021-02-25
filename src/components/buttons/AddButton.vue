<template>
  <button class="add-button" />
</template>

<script>
export default {
  name: 'AddButton'
}
</script>

<style scoped>
.add-button {
  width: 50px;
  height: 50px;
  border-radius: 15px;
  background-color: green;
  border: none;
  outline: none;

  transition: background-color 0.2s;
}

.add-button:hover {
  background-color: #00d600
}

.add-button::before {
  content: "+";
  padding: 0;
  margin: 0;
  height:50px;
  width:50px;
  font-size:40px;
  display:flex;
  flex-direction:row;
  align-items:center;
  justify-content:center;
  font-weight: 400;
  color:white;
}
</style>