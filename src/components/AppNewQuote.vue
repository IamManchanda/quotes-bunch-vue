<template>
  <form action="">
    <div class="grid-x grid-margin-x grid-padding-y">
      <div class="cell">
        <label><strong>Quote</strong></label>
        <textarea rows="3" v-model="quote"></textarea>
        <input type="submit" class="button primary" value="Add Quote" @click.prevent="createNew">
      </div>
    </div>
  </form>
  
</template>

<script>
export default {
  data() {
    return {
      quote: ''
    };
  },
  methods: {
    createNew() {
      this.$emit('quoteAdded', this.quote);
      this.quote = '';
    }
  }
}
</script>

<style lang="scss" scoped>
  
</style>