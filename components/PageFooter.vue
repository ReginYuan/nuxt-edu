<template>
	<div class="pageFooter">
		<div class="flex items-center justify-center py-5">
			<a href="#" v-for="i in 5" class="py-3">友情链接</a>
		</div>
		<div class="container border-t border-gray-700 flex items-center justify-center py-5">
			<small> Copyright @ 2022 dishait.cn 粤ICP备2020100536号 </small>
		</div>
	</div>
</template>
 
<script setup lang="ts">
</script>
 
<style lang="scss" scoped>
.pageFooter {
	@apply mt-auto bg-dark-400 text-gray-100;
}
</style>