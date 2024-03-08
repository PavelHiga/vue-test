<template>
	<button :class="classBtn">
		<slot></slot>
	</button>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
	width: String
})

const classBtn = computed(() => {
	return props.width === 'full' ? 'button__full' : 'button'
})
</script>

<style lang="scss" scoped>
@mixin button {
	height: fit-content;
	width: fit-content;
	border-radius: 15%;
	border-bottom: 3px solid rgb(146, 146, 146);
	padding: 12px 12px 10px 12px;
	background-color: rgb(237, 237, 237);
	&:hover {
		background-color: rgb(209, 209, 209);
	}

	&:active {
		background-color: rgb(237, 237, 237);
		border-bottom: none;
	}
}

.button {
	@include button;
}

.button__full {
	@include button;
	width: 100%;
	border-radius: 10px;
}
</style>
