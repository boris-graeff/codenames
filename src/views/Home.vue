<template>
  <div class="home">
    <h1>Codename</h1>
    <form @submit.prevent="createNewRoom">
      <p>Create new room</p>
      <button type="submit">Create</button>
    </form>
  </div>
</template>

<script>
export default {
  methods: {
    createNewRoom() {
      this.$router.push({ name: 'room', params: { slug: 'test'} })
    }
  }
}
</script>
