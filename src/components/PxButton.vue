<template>
	<button
		class="bg-transparent hover:bg-pink-500 text-pink-700 hover:text-white py-2 px-2 border border-pink-500 hover:border-transparent rounded"
		@click="buttonClick"
	>
		<slot></slot>
	</button>
</template>

<script>
export default {
	name: "PxButton",

	methods: {
		buttonClick() {
			this.$emit("click");
		},
	},
};
</script>