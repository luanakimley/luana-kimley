<template>
  <nav class="nav-bar">
    <div class="d-flex justify-content-center">
      <RouterLink to="/" class="mx-2 pink nav-link">home</RouterLink>
      <RouterLink to="/about" class="mx-2 pink nav-link">about</RouterLink>
      <RouterLink to="/projects" class="mx-2 pink nav-link">projects</RouterLink>
    </div>
  </nav>
</template>
<style scoped>
.nav-bar {
  margin: 10px;
  margin-top: 20px;
}

.nav-link {
  cursor: pointer;
  position: relative;
  transition: all 0.7s;
  padding: 5px 10px;
  border: 3px solid transparent;
  &:hover {
    border-bottom: 3px solid #2671bc;
    border-top: 3px solid #ffc612;
  }
}
</style>
