<template lang="html">
  <div class="">
    <h1>Energy</h1>
    <div class="">
      <energies-list :energies="energies"></energies-list>
    </div>
  </div>
</template>

<script>
import EnergiesList from './components/EnergiesList.vue'
export default {
  name: 'app',
  data() {
    return {
      energies: {},
      from: {},
      to: {}
    }
  },
  mounted() {
    fetch('https://api.carbonintensity.org.uk/generation')
    .then(res => res.json())
    .then(data => {
      this.energies = data.data.generationmix
      this.from = data.data.from
      this.to = data.data.to
    })
  },
  components: {
    "energies-list": EnergiesList
  },
  computed: {

  },
}
</script>

<style lang="css" scoped>
</style>
