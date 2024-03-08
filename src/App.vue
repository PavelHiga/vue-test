<template>
	<v-container class="d-flex flex-column h-screen justify-space-between">
		<VueHeader :user="user" />
		<VueInfo :info="info" />
		<VueAnswers />
	</v-container>
</template>

<script setup>
import VueAnswers from './components/VueAnswers.vue'
import VueHeader from './components/VueHeader.vue'
import VueInfo from './components/VueInfo.vue'

const user = {
	name: 'Anton',
	score: 1000
}

const info = {
	text: 'Whithc aboa asd',
	conditions: 'Choose the right answer'
}
</script>

<style scoped></style>
