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
  :position="[5, 5, 8]"
  :look-at="[0, 0, 0]"
  />
  <OrbitControls />
  <Suspense>
        <TheRobot />
    </Suspense>
    <TresMesh :rotation="[-Math.PI / 2, 0, 0]">
      <TresPlaneGeometry :args="[4, 4]" />
      <TresMeshBasicMaterial color="#444" />
    </TresMesh>
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