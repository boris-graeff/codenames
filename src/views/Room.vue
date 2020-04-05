<template>
  <div class="room">
    <h1>Room: {{ slug }}</h1>
  </div>
</template>

<script>
export default {
  props: {
    slug: {
      type: String
    }
  }
}
</script>
