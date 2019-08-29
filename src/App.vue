<template lang="html">
  <h1>Energy</h1>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      energies: {}
    }
  },
  mounted() {
    fetch('https://api.carbonintensity.org.uk/generation')
    .then(res => res.json())
    .then(data => this.energies = data)
  }
}
</script>

<style lang="css" scoped>
</style>
