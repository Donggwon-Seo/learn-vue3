<template>
	<div>
		<h2>반응형</h2>
		<p>{{ reactiveMessage }}</p>
		<button v-on:click="addReactiveMesssage">Add message</button>
		<h2>일반</h2>
		<p>{{ normalMessage }}</p>
	</div>
</template>

<script>
import { ref } from "vue";

export default {
	setup() {
		const reactiveMessage = ref("Reactive Message");

		const addReactiveMesssage = () => {
			reactiveMessage.value = reactiveMessage.value + "!";
		};

		const normalMessage = "Normal Message";

		return {
			reactiveMessage,
			normalMessage,
			addReactiveMesssage,
		};
	},
};
</script>

<style lang="scss" scoped></style>
