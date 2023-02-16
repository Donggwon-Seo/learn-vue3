<template>
	<div></div>
</template>

<script>
import { reactive, readonly } from "vue";

export default {
	setup() {
		const original = reactive({ count: 0 });

		const copy = readonly(original);

		// 원본이 변이되면 복사본에 의존하는 watch 도 트리거될 것 입니다.
		original.count++;

		return { copy };
	},
};
</script>

<style lang="scss" scoped></style>
