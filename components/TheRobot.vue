<script setup>
import { useGLTF } from '@tresjs/cientos';

const { scene: model } = await useGLTF(
  // 'https://raw.githubusercontent.com/Tresjs/assets/main/models/gltf/blender-cube.glb',
  'https://github.com/InesSorzano/tres-test/blob/main/models/robot_cup.gltf',
  { draco: true }
);
</script>

<template>
  <primitive :object="model" />
</template>
