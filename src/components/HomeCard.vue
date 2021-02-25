<template>
  <div class="home-card">
    <h3>{{ title }}</h3>
    <p>{{ value }}</p>
  </div>
</template>
<script>
export default {
  name: 'HomeCard',
  props: {
    title: {
      type: String,
      required: true,
    },
    value: {
      type: [String, Number],
      required: true,
    }
  }
}
</script>
<style scoped>
  .home-card {
    width: 320px;
    background-color: lightgreen;
    padding: 30px 40px;
    border-radius: 10px;
    text-align: center;
    font-size: 48px;
  }
</style>