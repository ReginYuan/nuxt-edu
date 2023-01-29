<template>
  <div class="body bg-gray-100 flex flex-col min-h-screen">
    <NavBar />
    <main class="container">
      <slot />
    </main>
    <PageFooter />
  </div>
</template>

<script setup lang="ts">
</script>

<style scoped>
.body {
  min-width: 1000px;
  /* @apply flex flex-col bg-gray-100 min-h-screen; */
}

</style>