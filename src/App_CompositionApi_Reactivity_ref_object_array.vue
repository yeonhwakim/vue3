<template>
	<div></div>
</template>

<script>
import { reactive, ref } from 'vue'

export default {
	setup() {
		const count = ref(0)
		count.value++

		// ref -> object
		const object = reactive({
			count,
		})
		console.log('reactive(object)', object.count) //unwarpping

		// ref -> array
		const array = reactive([count])
		console.log('reactive(array)', array[0].value)

		return {}
	},
}
</script>

<style lang="scss" scoped></style>
