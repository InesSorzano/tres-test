<script setup>
import { useGLTF } from '@tresjs/cientos';

// const { scene: model } = await useGLTF(
//   // 'https://raw.githubusercontent.com/Tresjs/assets/main/models/gltf/blender-cube.glb',
//   // 'https://raw.githubusercontent.com/InesSorzano/tres-test/refs/heads/main/models/robot_cup.gltf',
//   './models/Duck.gltf'
//   // { draco: true }
// );

const { nodes } = await useGLTF('models/robot_cup.glb', { draco: true })
console.log("nodes")
console.log(nodes)
const robot = nodes['Scene']
</script>

<template>
  <primitive :object="robot" />
</template>
