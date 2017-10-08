<template>
  <div class="cell small-6 medium-4 large-3">
    <div class="card radius shadow">
      <div class="card-section quote">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="scss" scoped>
.card {
  .card-section {
    font-family: 'Dancing Script', cursive;
    font-size: 1.5rem;
    color: #6e6e6e;
  }

  .quote {
    cursor: pointer;
    font-weight: 700;

    &:hover, &:focus {
      background-color: #ffe2e2;
    }
  }
}
</style>