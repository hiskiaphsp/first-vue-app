<template>
  <div class="min-h-screen bg-gray-800">
    <Navbar :navigation/>
  </div>
</template>

<script setup>
import Navbar from "./components/Navbar.vue";
const navigation = [
  { name: 'Dashboard', href: '#', current: true },
  { name: 'Team', href: '#', current: false },
  { name: 'Projects', href: '#', current: false },
  { name: 'Calendar', href: '#', current: false },
]
</script>
