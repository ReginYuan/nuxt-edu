<template>
	<div class="">公共列表{{ $route.params.type }} ~ {{ $route.name }}</div>
</template>
 
<script setup lang="ts">
import { useRoute } from 'vue-router'
const route = useRoute()
console.log(' $route.params.type', route.params.type)
</script>
 
<style lang="scss" scoped>
</style>