<template>
	<div>
		<v-row class="justify-end mt-4">
			<v-col cols="2" class="d-flex flex-column align-end gr-2 justify-center">
				<p>{{ user.name }}</p>
				<div class="d-flex gc-2">
					<p>{{ user.score }}</p>
					<img src="../assets/images/coin.png" alt="coin image" />
				</div>
			</v-col>
		</v-row>
	</div>
</template>

<script setup>
defineProps({
	user: {
		name: String,
		score: Number
	}
})
</script>

<style scoped></style>
