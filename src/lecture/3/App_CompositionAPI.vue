<template>
	<div>
		<h2>반응형</h2>
		<p>{{ reactiveMessage }}</p>
		<button v-on:click="addReactiveMesssage">Add message</button>
		<h2>일반</h2>
		<p>{{ normalMessage }}</p>
		<button v-on:click="addNormalMessage">Add message</button>
	</div>
</template>

<script>
import { onBeforeMount, onMounted, ref } from "vue";

export default {
	setup() {
		console.log("setup()");
		const reactiveMessage = ref("Reactive Message");

		const addReactiveMessage = () => {
			reactiveMessage.value = reactiveMessage.value + "!";
		};
		// console.log("isRef(reactiveMessage): ", isRef(reactiveMessage));

		let normalMessage = "Normal Message";
		const addNormalMessage = () => {
			normalMessage.value = normalMessage.value + "!";
		};
		// console.log("isRef(normalMessage): ", isRef(normalMessage));

		onMounted(() => {
			console.log("onMounted");
		});

		onBeforeMount(() => {
			console.log("onBeforeMount");
		});

		return {
			reactiveMessage,
			normalMessage,
			addReactiveMessage,
			addNormalMessage,
		};
	},
};
</script>

<style lang="scss" scoped></style>
