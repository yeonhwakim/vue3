<template>
	<p>author: {{ author }}</p>
	<p>year: {{ year }}</p>
	<p>title: {{ title }}</p>
	<p>description: {{ description }}</p>
	<p>price: {{ price }}</p>
</template>

<script>
import { reactive, toRef, toRefs } from 'vue'

export default {
	setup() {
		const book = reactive({
			author: 'Vue Team',
			year: '2020',
			title: 'Vue 3 Guide',
			description: '당신은 이 책을 지금 바로 읽습니다 ;)',
			price: '무료',
		})

		let { year, description } = book // 반응형이 해제됨
		let { author, title } = toRefs(book) // 반응형이 해제됨
		let price = toRef(book, 'price') // 한가지만 가져오고 싶을때

		return { year, description, author, title, price }
	},
}
</script>

<style lang="scss" scoped></style>
