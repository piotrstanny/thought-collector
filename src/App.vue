<template>
    <div class="container">
        <h1>Quote Collector</h1>
        <p>Collect your favourite quotes!</p>
        <QuoteGrid :quotes="quotes"/>
        <NewQuote/>
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
        }
    }
</script>

<style>
h1 {
    padding-top: 30px;
}
</style>
