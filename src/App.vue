<template>
  <div class="grid-container">
    <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
    <div class="grid-x grid-margin-x">
      <div class="cell">
        <div class="callout primary">
          <p class="text-center">Note: You can click on the quote anytime to delete it.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AppQuoteGrid from './components/AppQuoteGrid.vue';
import AppNewQuote from './components/AppNewQuote.vue';
import AppHeader from './components/AppHeader.vue';

export default {
  data() {
    return {
      quotes: [
        'Revolution did not necessarily involve sanguinary strife. It was not a cult of bomb and pistol.',
        'To call woman the weaker sex is a libel; it is man\'s injustice to woman.'
      ],
      maxQuotes: 8
    };
  },
  methods: {
    newQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert('Please delete Quotes First');
      }
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1)
    }
  },
  components: { AppQuoteGrid, AppNewQuote, AppHeader }
}
</script>

<style lang="scss">
  body { padding-top: 1rem; }
</style>
