<template>
    <div class="row">
        <Quote v-for="quote in quotes" :key="quote">
            {{quote}}
        </Quote>
    </div>
</template>

<script>
import Quote from './Quote'

export default {
    components: {
        Quote
    },
    props: ['quotes']
}
</script>

<style scoped>
    div {
        padding-top: 50px;
    }
</style>