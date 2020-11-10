<template>
  <div>
    {{ num }}
  </div>
</template>

<script>
export default {
  name: 'findBodyPage',
  data () {
    return {
      num: this.$route.query.commentNumber
    }
  }
}
</script>

<style>

</style>
