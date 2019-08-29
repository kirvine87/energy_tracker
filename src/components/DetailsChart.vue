<template lang="html">
  <p>chart</p>
</template>

<script>
export default {
  name: 'details-chart',
  props: ['energies'],
  computed: {
    chartData() {
      return this.energies.map(Object.values)
    }
  }
}
</script>

<style lang="css" scoped>
</style>
