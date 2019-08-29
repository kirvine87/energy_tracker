<template lang="html">
  <div class="">
    <h1>Energy</h1>
    <div class="">
      <energies-list></energies-list>
    </div>
  </div>
</template>

<script>
import EnergiesList from './components/EnergiesList.vue'
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
  },
  components: {
    "energies-list": EnergiesList
  }
}
</script>

<style lang="css" scoped>
</style>
