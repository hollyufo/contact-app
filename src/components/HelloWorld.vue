<script setup>
import { ref } from 'vue'

defineProps({
  msg: {
    type: String,
    default: 'Hello Vue 3 + Vite'
  }
})

const count = ref(0)

function incriment() {
  console.log('incriment')
  count.value++
}
</script>

<template>
  <h1 class="text-3xl font-bold underline">{{ msg }}</h1>

  <p>
    Recommended IDE setup:
    <a class="pt-4 text-pink-700" href="https://code.visualstudio.com/" target="_blank">VSCode</a>
    +
    <a href="https://github.com/johnsoncodehk/volar" target="_blank">Volar</a>
  </p>

  <p>
    <a href="https://vitejs.dev/guide/features.html" target="_blank">
      Vite Documentation
    </a>
    |
    <a class="link" href="https://v3.vuejs.org/" target="_blank">Vue 3 Documentation</a>
  </p>

  <button type="button" @click="()=>incriment()">count is: {{ count }}</button>
  <p>
    Edit
    <code>components/HelloWorld.vue</code> to test hot module replacement.
  </p>
</template>