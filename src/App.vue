<template>
  <div class="container">
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
    <div class="col-sm-12 text-center">
      <div class="alert alert-info">Info: click on a quote to delete it</div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue';

export default {
  data: function() {
    return {
      quotes: ['My first quote', 'This is just a quote'],
      maxQuotes: 10
    }
  },
  components: {
    'app-quote-grid': QuoteGrid,
    'app-new-quote': NewQuote
  },
  methods: {
    newQuote(quote) {
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  }
}
</script>
