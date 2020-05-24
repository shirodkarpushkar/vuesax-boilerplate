<script>
import Layout from '@layouts/main'

export default {
  page: {
    title: 'Page timeout',
    meta: [
      { name: 'description', content: 'The page timed out while loading.' },
    ],
  },
  components: { Layout },
}
</script>

<template>
  <div>
    Timeout
  </div>
</template>

<style lang="scss" module>
.title {
  text-align: center;
}
</style>
