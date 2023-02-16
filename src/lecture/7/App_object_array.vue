<template>
	<div></div>
</template>

<script>
import { reactive, ref } from "vue";

export default {
	setup() {
		// ref-> Object
		const count = ref(0);
		const state = reactive({
			count,
		});
		console.log(state.count);
		console.log(count.value);
		count.value++;

		// ref-> Array
		const message = ref("Hello");
		const arr = reactive([message]);
		console.log("arr[0]: ", arr[0].value);

		// Destructuring
		return {};
	},
};
</script>

<style lang="scss" scoped></style>
