<template>
  <div class="">
    ่่ฏๅ่กจ{{ $route.params.page }}
  </div>
</template>
 
<script setup>
import { useRoute } from 'vue-router';
const route = useRoute()
</script>
 
<style lang="scss" scoped>

</style>