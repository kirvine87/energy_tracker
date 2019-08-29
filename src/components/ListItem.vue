<template lang="html">
  <div class="">
      <li>{{energy.fuel}}: {{energy.perc}}%</li>
  </div>

</template>

<script>
export default {
  name: 'list-item',
  props: ['energy'],
}
</script>

<style lang="css" scoped>
</style>
