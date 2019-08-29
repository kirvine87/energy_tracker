<template lang="html">
  <div class="">
    <ul>
      <list-item v-for="(energy, index) in energies" :energy="energy" :key="index"></list-item>
    </ul>
  </div>
</template>

<script>
import ListItem from './ListItem.vue'
export default {
  name: 'energies-list',
  props: ['energies'],
  components: {
    "list-item": ListItem
  }
}
</script>

<style lang="css" scoped>
</style>
