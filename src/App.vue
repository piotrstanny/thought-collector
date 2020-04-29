<template>
    <div class="container-fluid">
        <h1>Quote Collector</h1>
        <p>Collect your favourite quotes!</p>
        <NewQuote @quoteAdded="newQuote($event)"/>
        <div class="row justify-content-center">
			<div class="col-xs-12 col-sm-6">
				<div class="alert alert-danger">Info: Click on the Quote to delete it</div>
			</div>
		</div>
        <QuoteGrid :quotes="quotes"/>

    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid'
    import NewQuote from './components/NewQuote'

    export default {
        components: {
            QuoteGrid,
            NewQuote
        },
        data() {
            return {
                maxQuotes: 10,
                quotes: [
                    'What gets measured gets managed. Pay attention to all factors, that\'s the way to succeed.'
                ]
            }
        },
        methods: {
            newQuote(quote) {
                this.quotes.push(quote)
            }
        }
    }
</script>

<style>
h1 {
    padding-top: 30px;
}
.container-fluid {
    justify-content: center;
    text-align: center;
    justify-items: center;
    margin: 0 auto;
}
</style>
