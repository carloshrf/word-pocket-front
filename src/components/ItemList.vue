<template>
  <div class="container">
    <div class="content">
      <div class="values">
        <p>{{ phrase }}</p>
        <span>{{ translated }}</span>
      </div>
      <div class="infos">
        2 keywords
      </div>
      <div class="right-arrow"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ItemList',
  props: {
    phrase: String,
    translated: String
  }
}
</script>

<style scoped>
.container {
  width: 100%;
  cursor: pointer;
  transition: transform 0.2s;
  box-shadow: 1px 5px 14px 2px rgba(0,0,0,0.2)
}

.container:hover {
  transform: scale(1.01);
}

.content {
  width: 100%;
  display: flex;
  justify-content: space-between;
  position: relative;
  padding: 15px 20px;
  background-color: #FFF;
}

.values p {
  font-weight: 700;
}

.values span {
  font-style: italic;
  font-size: 16px;
  color: #c3c3c3;
}

.infos {
  display: flex;
  align-items: center;
  padding-right: 20px;
}

.right-arrow {
  position: absolute;
  width: 10px;
  height: 10px;
  border-right: 3px solid #000;
  border-bottom: 3px solid #000;
  right: 20px;
  top: calc(50% - 5px);
  transform: rotate(-45deg);
}
</style>