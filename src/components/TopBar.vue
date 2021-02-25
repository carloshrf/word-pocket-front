<template>
  <div class="top-bar-container">
    <div class="content">
      <img src="../assets/images/logo.svg" alt="logo">

      <label class="switch">
        <input type="checkbox" />
        <span class="slider"></span>
      </label>

    </div>
  </div>
</template>

<script>
export default {
  name: 'TopBar'
}
</script>

<style scoped>
.top-bar-container {
  width: 100%;
  height: 50px;
  border-radius: 0 0 60px 60px;
  background-color: wheat;
}

.top-bar-container .content {
  padding: 5px 50px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.top-bar-container .content img {
  height: 40px;
}

/* Switch */

.switch {
  position: relative;
  display: inline-block;
  width: 50px;
  height: 26px;
}

.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  right: 0;
  left: 0;
  bottom: 0;
  background-color: #CCC;
  border-radius: 34px;
  transition: .4s;
}

.slider:before {
  position: absolute;
  content: "";
  height: 20px;
  width: 20px;
  left: 3px;
  bottom: 3px;
  background-color: #FFF;
  border-radius: 50%;
  transition: .4s;
}

input:checked + .slider {
  background-color: #2196F3;
}

input:checked + .slider::before {
  transform: translateX(24px);
}

</style>