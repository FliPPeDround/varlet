<template>
  <div :class="classes(n(), [hovering, n('--hovering')], [focusing, n('--focusing')])"></div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { props } from './props'
import { createNamespace } from '../utils/components'

const { name, n, classes } = createNamespace('hover-overlay')

export default defineComponent({
  name,
  props,
  setup: () => ({
    n,
    classes,
  }),
})
</script>

<style lang="less">
@import '../styles/common';
@import './hoverOverlay';
</style>
