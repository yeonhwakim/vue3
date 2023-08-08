<template>
	<div>
		<!--템플릿 문자열로 보여주기-->
		<p>{{ message }}</p>
	</div>
</template>

<script>
export default {
	setup() {
		// create 되기전 실행
		const message = 'Hello VUE3' // 선언하고

		return {
			message, // 리턴해서
		}
	},
}
</script>

<style lang="scss" scoped></style>
