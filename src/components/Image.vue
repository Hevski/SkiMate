<template lang="html">

</template>

<script>
export default {
  props:['type', 'width'],
  computed: {
    style () {
      return 'background-image: url(' + this.type + '), width: (' + this.width +');'
    }
  }
}
</script>

<style lang="css" scoped>
</style>
