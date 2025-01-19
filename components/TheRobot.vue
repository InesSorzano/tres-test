<script setup>
import { useGLTF } from '@tresjs/cientos';

const { nodes } = await useGLTF('models/robot_cup.glb', { draco: true })
console.log("nodes")
console.log(nodes)
const robot = nodes['Scene']

function changeColor(ev) {
  if (ev) {
    console.log(ev.object)
    if(ev.object.name=="Cube"){
      ev.object.visible = false
    }
    ev.object.material.color.set('#26F03A');
  }
}
</script>

<template>
  <primitive :object="robot" @click="changeColor"/>
</template>
