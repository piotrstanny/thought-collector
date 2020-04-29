<template>
    <div class="container-fluid">
        <h1>Quote Collector</h1>
        <p>Collect your favourite quotes!</p>
        <NewQuote @quoteAdded="newQuote($event)"/>
        <ProgressBar :quoteCount="quotes.length" :maxQuote="maxQuote"></ProgressBar>
        <hr>
        <div class="row justify-content-center">
			<div class="col-xs-12 col-sm-6">
				<div class="alert alert-danger">Info: Click on the Quote to delete it</div>
			</div>
		</div>
        <QuoteGrid :quotes="quotes" @quoteDeleted="deleteQuote($event)"></QuoteGrid>

    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid'
    import NewQuote from './components/NewQuote'
    import ProgressBar from './components/ProgressBar'
    

    export default {
        components: {
            QuoteGrid,
            NewQuote,
            ProgressBar
        },
        data() {
            return {
                maxQuotes: 10,
                quotes: [
                    'The only bad workout is the one that didn\'t happen',
                    'What gets measured gets managed. Pay attention to all factors, that\'s the way to succeed.', 'My job here is to make you do what you don’t wanna do, so you can be what you wanna be.', 'Insanity: Doing the same thing over and over again and expecting different results.', 'Success is the sum of small efforts—repeated day-in and day-out.'
                ],
                maxQuote: 10
            }
        },
        methods: {
            newQuote(quote) {
                if (this.quotes.length >= this.maxQuotes) {
                    alert("\nYou reached limit of quotes!\n\nDelete some before adding new.")
                } else {
                    this.quotes.push(quote)
                }
            },
            deleteQuote(index) {
                this.quotes.splice(index, 1);
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
    margin-bottom: 50px;
}
</style>
