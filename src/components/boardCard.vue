<template>
  <div class="card">
    {{ card.word }}
  </div>
</template>

<script>
export default {
  props: {
    card: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped lang="less">
.card {
  height: 12vh;
  text-align: center;
  border-radius: 10px;
  text-transform: uppercase;
  font-weight: bold;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
  background: white;
  box-shadow: 0 3px 9px -5px grey;
}
</style>
