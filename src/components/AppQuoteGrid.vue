<template>
  <div class="grid-x grid-margin-x grid-padding-y">
    <app-quote v-for="(quote, index) in quotes" @click.native="deleteQuote(index)">
      {{ quote }}
    </app-quote>
  </div>
</template>

<script>
import AppQuote from './AppQuote.vue';

export default {
  props: ['quotes'],
  components: { AppQuote },
  methods: {
    deleteQuote(index) {
      this.$emit('quoteDeleted', index);
    }
  }
}
</script>

<style lang="scss" scoped>
  
</style>