<template>
  <div>
    <h3>Quotes Added {{ quoteCount }} / {{ maxQuotes }}</h3>
    <progress class="progress" :value="(quoteCount/maxQuotes)*100" max="100" aria-describedby="example-caption-2"></progress>
  </div>
</template>

<script>
export default {
  props: ['quoteCount', 'maxQuotes'],
  methods: {
    
  }
}
</script>
