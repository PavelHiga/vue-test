<template>
	<div>
		<v-row class="flex justify-space-between bg-color-red px-10">
			<v-col v-for="(item, index) in data" :key="index" cols="3.5">
				<VueButton @click="answerClick(item)" width="full">{{
					item
				}}</VueButton>
			</v-col>

			<v-col cols="1"
				><VueButton @click="checkClick" width="full">Check</VueButton></v-col
			>
		</v-row>
	</div>
</template>

<script setup>
import { ref } from 'vue'
import VueButton from './VueButton.vue'

const data = ['a', 'b', 'c']

const activeAnswer = ref(null)

const answerClick = item => {
	activeAnswer.value = item
}

const checkClick = () => {
	console.log(activeAnswer.value)
}
</script>

<style scoped></style>
