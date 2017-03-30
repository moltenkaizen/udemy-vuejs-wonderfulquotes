<template>
    <div class="row">
        <div v-for="quote in quotes">
        <app-quote :quote="quote" :deleteQuote="deleteQuote" ></app-quote>
            </div>
    </div>
</template>

<script>
    import Quote from './Quote.vue'
    export default {
        props: ['quotes', 'deleteQuote'],
        components: {
            appQuote: Quote
        }

    }
</script>

<style>
</style>