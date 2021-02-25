<template>
  <div class="container" @click="handleModal">
    <div class="content">
      <div class="close" @click="handleModal(false)" />
      <h2>{{ title }}</h2>
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Modal',
  props: {
    title: String,
    handleModal: Function
  }
}
</script>

<style scoped>
.container {
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.2);
}

.content {
  width: 460px;
  position: fixed;
  background-color: darkviolet;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  border-radius: 20px;
  padding: 40px;
}

.close {
  position: absolute;
  height: 25px;
  width: 25px;
  top: 15px;
  right: 15px;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 50%;
  background-color: rgba(0, 0, 0, 0.2);
  transform: rotate(45deg);
  cursor: pointer;
}

.close::after {
  content: "";
  top: 10px;
  left: 2px;
  width: 19px;
  border-bottom: 3px solid #FFF;
  border-radius: 2px;
  position: absolute;
}

.close::before {
  content: "";
  top: 10px;
  left: 2px;
  width: 19px;
  border-bottom: 3px solid #FFF;
  border-radius: 2px;
  position: absolute;
  transform: rotate(90deg)
}

</style>