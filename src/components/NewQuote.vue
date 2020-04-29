<template>
<div>
	<form action="">
		<div class="row justify-content-center">
			<div class="col-sm-6 form-group">
				<label for="quote">Write new Quote:</label>
				<textarea name="quote" id="quote" cols="10" rows="3" class="form-control" v-model="quote"></textarea>
			</div>
		</div>
		<div class="row justify-content-center">
			<div class="col-sm-6 form-group">
				<button type="button" class="btn btn-dark" @click="createNew">Add Quote</button>
			</div>
		</div>
	</form>
</div>
</template>

<script>
export default {
    data: function() {
		return {
			quote: ''
		}
	},
	methods: {
		createNew() {
			this.$emit('quoteAdded', this.quote);
			this.quote = ''
		}
	}
}
</script>

<style scoped>
form {
	justify-content: center;
    text-align: center;
    justify-items: center;
	margin: 0 auto;
}
</style>