<template>
<div>
	<form action="">
		<div class="row">
			<div class="col-sm-6 offset-sm-3 form-group">
				<label for="quote">Add new Quote:</label>
				<textarea name="quote" id="quote" cols="10" rows="5" class="form-control" v-model="quote"></textarea>
			</div>
		</div>
		<div class="row">
			<div class="col-sm-6 offset-sm-3 form-group">
				<button type="button" class="btn btn-primary" @click="createNew">Add Quote</button>
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

</style>