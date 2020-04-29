<template>
<div class="bar-container">
	<h4>Number of Quotes added:</h4>
	<div class="progress" style="height: 30px;">
	<div class="progress-bar" 
	role="progressbar" 
	aria-valuenow="0" 
	aria-valuemin="0" 
	aria-valuemax="100"
	:style="{ width: barWidth() }"
	>{{ quoteCount }} out of {{ maxQuote }}</div>
	</div>
</div>
</template>

<script>
export default {
	props: ['quoteCount', 'maxQuote'],
	methods: {
		barWidth() {
			return this.quoteCount / this.maxQuote * 100 + '%'
		}
	}
}
</script>

<style scoped>
.progress {
	font-size: 0.9rem;
}
.bar-container {
	margin-bottm: 20px;
}
</style>