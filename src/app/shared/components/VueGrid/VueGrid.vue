<template>
  <div :class="['vue-grid', $style.grid]">
    <slot />
  </div>
</template>

<script lang="ts">
  export default {};
</script>

<style lang="scss" module>
  @import "../../styles";

  .grid {
    display:        flex;
    flex-direction: row;
    flex-wrap:      wrap;
    max-width:      425px;
    margin:         0 auto;
    position:       relative;

    @include media(tabletPortrait) {
      max-width: $screen-tablet-portrait;
      padding:   0 $screen-tablet-portrait-gutter;
    }

    @include media(tabletLandscape) {
      max-width: $screen-tablet-landscape;
      padding:   0 $screen-tablet-landscape-gutter;
    }

    @include media(smallDesktop) {
      max-width: $screen-small-desktop;
      padding:   0 $screen-small-desktop-gutter;
    }

    @include media(largeDesktop) {
      max-width: $screen-large-desktop;
      padding:   0 $screen-large-desktop-gutter;
    }
  }
</style>
