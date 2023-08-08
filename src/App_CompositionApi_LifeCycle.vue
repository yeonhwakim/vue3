<template>
	<div></div>
</template>

<script>
import { onBeforeMount, onMounted } from 'vue'

export default {
	setup() {
		console.log('setup')

		onMounted(() => {
			console.log('onMounted')
		})

		onBeforeMount(() => {
			console.log('onBeforeMounted')
		})
	},
}
</script>

<style lang="scss" scoped></style>
