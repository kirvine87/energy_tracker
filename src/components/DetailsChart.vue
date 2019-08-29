<template lang="html">
  <div class="">
    <GChart
      type="ColumnChart"
      :data="chartData"
      :options="chartOptions"
    />
  </div>
</template>

<script>
export default {
  name: 'details-chart',
  props: ['energies'],
  data() {
    return {
      chartOptions: {
        chart:{
          title: 'Fuel Usage',
          subtitle: 'UK'
        }
      }
    }
  },
  computed: {
    chartData () {
      const rawData = this.energies.map(Object.values)
      rawData.unshift(['fuel', 'perc'])
      return rawData
    }
  }
}
</script>

<style lang="css" scoped>
</style>
