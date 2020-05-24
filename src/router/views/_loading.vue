<script>


export default {
  page: {
    title: 'Loading page...',
    meta: [{ name: 'description', content: 'Loading page...' }],
  },
  components: {  },
}
</script>

<template>
  <div>
    Loading
  </div>
</template>

<style lang="scss" module>
@import '@design';

.loadingIcon {
  @extend %typography-xxlarge;

  display: block;
  margin: 0 auto;

  // stylelint-disable-next-line selector-class-pattern
  &:global(.v-enter-active) {
    transition: opacity 1s;
  }
  // stylelint-disable-next-line selector-class-pattern
  &:global(.v-enter) {
    opacity: 0;
  }
}
</style>
