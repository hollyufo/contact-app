<script setup>
import { ref, computed } from 'vue'
import Home from './pages/Home.vue'
import Login from './pages/Login.vue'
import './index.css'

const routes = {
  '/': Home,
  '/login': Login
}

const currentPath = ref(window.location.hash)

window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash
})

const currentView = computed(() => {
  return routes[currentPath.value.slice(1) || '/']
})
</script>

<template>
  <a href="#/">Home</a> |
  <a href="#/login">About</a> |
  <component :is="currentView" />
</template>