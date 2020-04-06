<template>
  <div class="home">
    <header>
      <h1>
        <span>Code</span>
        <span>names</span>
      </h1>
    </header>
    <form @submit.prevent="createNewRoom">
      <button type="submit">Let's play !</button>
    </form>
  </div>
</template>

<script>
export default {
  methods: {
    createNewRoom () {
      this.$router.push({ name: 'room', params: { slug: 'test' } })
    }
  }
}
</script>

<style scoped lang="less">
header {
  display: flex;
  justify-content: center;
  align-items: center;
}

h1 {
  border: 4px solid;
  text-transform: uppercase;
  margin: auto;
  font-size: 40px;

  span {
    display: block;
    padding: 6px 20px;

    &:last-child {
      background: #2c3e50;
      color: white;
    }
  }
}

button {
  margin-top: 20px;
  padding: 6px 10px;
  font-size: 20px;
  border-radius: 3px;
  border: 3px solid;
}
</style>
