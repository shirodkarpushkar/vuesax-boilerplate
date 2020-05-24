<template>
  <div>
    404 page
  </div>
</template>

<script>
export default {
  name: 'FourOhFour',

  created() {
    this.$ssrContext && this.$ssrContext.res.status(404)
  },
}
</script>
