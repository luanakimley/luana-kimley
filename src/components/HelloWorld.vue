<script setup lang="ts">
import NavBar from './NavBar.vue'

// defineProps<{
//   msg: string
// }>()
</script>

<template>
  <NavBar />

  <div class="d-flex justify-content-center align-items-center flex-column vh-100">
    <img
      class="rounded-circle mb-4"
      alt="Luana picture"
      src="@/assets/profile.jpg"
      width="175"
      height="175"
    />

    <h3 class="fw-bold outline yellow text-uppercase">Hello World!</h3>
    <h1 class="mb-4">I'm <strong class="blue">Luana</strong></h1>

    <div class="d-flex flex-column text-center">
      <RouterLink class="my-3 pink nav-link" to="/about">about me</RouterLink>
      <RouterLink class="pink nav-link" to="/projects">my projects</RouterLink>
    </div>
  </div>
</template>

<style scoped>
.vh-100 {
  height: 100vh;
}

.nav-link {
  cursor: pointer;
  position: relative;
  padding: 10px 20px;
  background: white;
  border-top-right-radius: 10px;
  border-bottom-left-radius: 10px;
  transition: all 1s;
  &:after,
  &:before {
    content: ' ';
    width: 10px;
    height: 10px;
    position: absolute;
    border: 0px solid #fff;
    transition: all 1s;
  }
  &:after {
    top: -1px;
    left: -1px;
    border-top: 3px solid #ffc612;
    border-left: 3px solid #2671bc;
  }
  &:before {
    bottom: -1px;
    right: -1px;
    border-bottom: 3px solid #ffc612;
    border-right: 3px solid #2671bc;
  }
  &:hover {
    border-top-right-radius: 0px;
    border-bottom-left-radius: 0px;
    &:before,
    &:after {
      width: 100%;
      height: 100%;
    }
  }
}
</style>
