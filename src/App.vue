<template>
    <div class="container">
    <h1>Quote Collector</h1>
    <p>Collect your favourite quotes!</p>
    <QuoteGrid :quotes="quotes"/>
    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid'

    export default {
        components: {
            QuoteGrid
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
</style>
