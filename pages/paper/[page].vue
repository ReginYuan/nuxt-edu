<template>
	<div class="">考试列表{{ $route.params.page }} -{{ $route.name }}</div>
</template>
 
<script setup>
import { useRoute } from 'vue-router'
const route = useRoute()
</script>
 
<style lang="scss" scoped>
</style>