<template>
	<div>
		<button @click="() => reactiveRef.count++">
			{{ `${reactiveRef.count}` }}
		</button>
	</div>
</template>

<script>
import { reactive } from 'vue'

export default {
	setup() {
		const reactiveRef = reactive({ count: 0 })
		console.log(reactiveRef.count) // 0
		reactiveRef.count++
		console.log(reactiveRef.count) // 1

		return {
			reactiveRef,
		}
	},
}
</script>

<style lang="scss" scoped></style>
