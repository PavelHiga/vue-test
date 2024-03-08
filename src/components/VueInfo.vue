<template>
	<div class="d-flex flex-column h-50 align-content-space-between">
		<v-row align="center" class="justify-space-between mt-10">
			<v-col cols="4" class="d-flex justify-start">
				<VueButton>
					<img src="../assets/images/close_btn.png" alt="close button" />
				</VueButton>
			</v-col>
			<v-col cols="4">
				<div>
					<p class="mb-5">{{ info.conditions }}</p>
					<h1>{{ info.text }}</h1>
				</div>
			</v-col>
			<v-col cols="4" class="d-flex justify-end">
				<VueButton>
					<img src="../assets/images/bulb.png" alt="hint image" />
				</VueButton>
			</v-col>
		</v-row>
		<v-row align="center" class="justify-center">
			<v-col cols="4">
				<img
					class="w-100"
					src="../assets/images/task_img.png"
					alt="task image"
				/>
			</v-col>
		</v-row>
	</div>
</template>

<script setup>
import VueButton from './VueButton.vue'

defineProps({
	info: {
		text: String,
		conditions: String
	}
})
</script>

<style scoped></style>
