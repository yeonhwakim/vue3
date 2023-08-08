<template>
	<div>
		<button @click="() => primitiveRef++">
			{{ `원시값 ${primitiveRef}` }}
		</button>
	</div>
</template>

<script>
import { ref } from 'vue'

export default {
	setup() {
		const primitiveRef = ref(0)
		console.log(primitiveRef.value) // 0
		primitiveRef.value++
		console.log(primitiveRef.value) // 1

		return {
			primitiveRef,
		}
	},
}
</script>

<style lang="scss" scoped></style>
