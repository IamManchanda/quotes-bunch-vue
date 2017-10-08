<template>
  <div class="grid-x grid-margin-x">
    <div class="cell">
      <h3>No. of Quotes Added</h3>
      <div class="progress" role="progressbar" tabindex="0" :aria-valuenow="(quoteCount/maxQuotes) * 100" aria-valuemin="0" :aria-valuetext="(quoteCount/maxQuotes) * 100 + ' percent'" aria-valuemax="100">
        <div class="progress-meter" :style="{ width: (quoteCount/maxQuotes) * 100 + '%' }">
          <p class="progress-meter-text">
            {{ quoteCount }} / {{ maxQuotes }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: ['quoteCount', 'maxQuotes']
  }
</script>

<style lang="scss" scoped>
  .progress {
    height: 1.35rem;
    .progress-meter {
      .progress-meter-text {
        font-size: 0.9rem;
      }
    }
  }
</style>