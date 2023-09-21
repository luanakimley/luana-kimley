<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="d-flex justify-content-center align-items-center flex-column vh-100">
    <img
      class="rounded-circle mb-4"
      alt="Luana picture"
      src="@/assets/profile.jpg"
      width="150"
      height="150"
    />

    <h1 class="green">Hi There!</h1>
    <h3 class="mb-4">I'm Luana</h3>

    <RouterLink class="" to="/about">About Me</RouterLink>
    <RouterLink to="/projects">My Projects</RouterLink>
  </div>
</template>

<style scoped>
.vh-100 {
  height: 100vh;
}
</style>
