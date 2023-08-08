<template>
	<div>
		<h1>텍스트 보간법</h1>
		<p>{{ message }}</p>
		<p v-once>{{ message }}</p>
		<button @click="() => message + '!'">Add message</button>
		<hr />
		<h1>v-html</h1>
		<p>{{ rawHtml }}</p>
		<p v-html="rawHtml"></p>
		<hr />
		<h1>속성 바인딩</h1>
		<div v-bind:title="dynamicTitle">마우스를 올려보세요</div>
		<input type="text" value="홍길동" v-bind:disabled="isInputDisabled" />
		<input v-bind="attrs" />
		<hr />
		<h1>JAVASCRIPT</h1>
		{{ message.split('').reverse().join('') }} <br />
		{{ isInputDisabled ? 'Yes' : 'No' }}
	</div>
</template>

<script>
import { ref } from 'vue'

export default {
	setup() {
		const message = ref('Hello')
		const rawHtml = ref('<strong>Hello<strong>')
		const dynamicTitle = ref('Hello')
		const isInputDisabled = ref(false)
		const attrs = ref({
			type: 'text',
			value: '12345',
			disabled: true,
		})

		return { message, rawHtml, dynamicTitle, isInputDisabled, attrs }
	},
}
</script>

<style lang="scss" scoped></style>
