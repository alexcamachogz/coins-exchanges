<template>
	<button
		class="bg-transparent hover:bg-pink-500 text-pink-700 hover:text-white py-2 px-2 border border-pink-500 hover:border-transparent rounded"
		@click="buttonClick"
	>
		<beat-loader :loading="isLoading" :color="'#C83280'" :size="8" />
		<span v-show="!isLoading"><slot></slot></span>
	</button>
</template>

<script>
export default {
	name: "PxButton",

	props: {
		isLoading: {
			type: Boolean,
			default: false,
		},
	},

	methods: {
		buttonClick() {
			this.$emit("click");
		},
	},
};
</script>
