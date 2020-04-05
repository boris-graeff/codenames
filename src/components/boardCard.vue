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
  padding: 20px;
  text-align: center;
  border: 1px solid;
  border-radius: 10px;
}
</style>
