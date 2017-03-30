<template>
    <div class="container">
        <app-header :maxQuotes="maxQuotes" :numQuotes="numQuotes" ></app-header>
        <app-new-quote :addQuote="addQuote"></app-new-quote>
        <app-quotes :quotes="quotes" :deleteQuote="deleteQuote" ></app-quotes>
    </div>
</template>

<script>
    import Header from './components/Header.vue'
    import NewQuote from './components/NewQuote.vue'
    import Quotes from './components/Quotes.vue'
    export default {
        data() {
            return {
                maxQuotes: 10,
                quotes: ['Super Duper Quote']
            }
        },
        methods: {
          addQuote(quote) {
              if (this.quotes.length < this.maxQuotes){
                  if (quote.length > 0 )this.quotes.push(quote)
              } else {
                  alert(`Max quotes of ${this.maxQuotes} reached`)
              }
          },
            deleteQuote(quote) {
              let index = this.quotes.indexOf(quote);
              this.quotes.splice(index, 1);
            }
        },
        computed: {
          numQuotes() {
              return this.quotes.length
          }
        },
        components: {
            appHeader: Header,
            appNewQuote: NewQuote,
            appQuotes: Quotes
        }
        
    }
</script>

<style>
</style>
