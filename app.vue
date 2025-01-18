<script setup lang="ts">
import { TresCanvas } from '@tresjs/core'
import { OrbitControls } from '@tresjs/cientos'

import TheRobot from './components/TheRobot.vue';
</script>

<template>
  <TresCanvas
  clear-color="#82DBC5"
  window-size
  shadows alpha
  >
  <TresPerspectiveCamera
  :position="[6, 6, 6]"
  :look-at="[0, 0, 0]"
  />
  <OrbitControls />
  <Suspense>
        <TheRobot />
    </Suspense>
    <!-- <TresMesh>
      <TresBoxGeometry :args="[1, 1, 1]" />
      <TresMeshBasicMaterial color="orange" />
    </TresMesh> -->
    <TresAmbientLight :intensity="5" />
  </TresCanvas>
</template>

<style>
html,
body {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
}
#app {
  height: 100%;
  width: 100%;
}
</style>