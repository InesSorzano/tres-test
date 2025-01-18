<script setup>
import { useGLTF } from '@tresjs/cientos';

const { nodes } = await useGLTF('models/robot_cup.glb', { draco: true })
console.log("nodes")
console.log(nodes)
const robot = nodes['Scene']
</script>

<template>
  <primitive :object="robot" />
</template>
