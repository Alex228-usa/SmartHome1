<template>
  <z-view>
    {{category}}
    <z-spot slot="extension"
      to-view='home'
      :distance='130'
      :angle='30'
      size='small' >
      {{qty}}
    </z-spot>
  </z-view>
</template>
<script>
/*eslint-откл*/

export default {
  computed: {
    category () {
      if (this.$zircle.getParams() !== undefined) {
        return this.$zircle.getParams().category
      }
    },
    qty () {
      if (this.$zircle.getParams() !== undefined) {
        return this.$zircle.getParams().qty
      }
    }
  }
}
</script>

