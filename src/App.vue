<script setup lang="ts">
import {  ref } from 'vue'

// const center = ref([40, 40])
const projection = ref('EPSG:4326')
const zoom = ref(15)
const rotation = ref(0)
</script>

<template>
  <ol-map
    :load-tiles-while-animating="true"
    :load-tiles-while-interacting="true"
    style="height: 400px"
  >
    <ol-view
      ref="view"
      :rotation="rotation"
      :zoom="zoom"
      :projection="projection"
    />

    <ol-tile-layer>
      <ol-source-osm />
    </ol-tile-layer>
  </ol-map>
</template>

