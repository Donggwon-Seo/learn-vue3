<template>
	<div>
		<div :style="styleObject">
			Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus,
			accusantium consectetur deleniti eligendi eumfugit iure obcaecati quae
			quia, quod repellat saepe suscipit veniam! A aperiam dolor eum nihil
			quidem.
		</div>
		<button v-on:click="fontSize++">+</button>
		<button v-on:click="fontSize--">-</button>
	</div>
</template>

<script>
import { computed, ref } from "vue";

export default {
	setup() {
		// const styleObject = reactive({
		// 	color: "red",
		// 	fontSize: "13px",
		// });
		const fontSize = ref(13);
		const styleObject = computed(() => {
			return {
				color: "red",
				fontSize: fontSize.value + "px",
			};
		});
		return { styleObject, fontSize };
	},
};
</script>

<style lang="scss" scoped></style>
