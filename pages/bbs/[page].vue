<template>
  <div class="">
    问答社区 {{ $route.params.bbs_id }}~ {{ $route.params.page }}
  </div>
</template>
 
<script setup>
import { useRoute } from 'vue-router';
const route = useRoute()
console.log(' $route.params.bbs_id', route.params.bbs_id)
</script>
 
<style lang="scss" scoped>

</style>