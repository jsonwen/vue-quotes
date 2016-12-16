<template>
  <div class="">
    <form style="margin: 20px 0;">
      <div>
        <label>Quote</label>
        <textarea class="form-control" rows="3" v-model="quote"></textarea>
      </div>
      <div class="row" style="margin-left:0px;">
        <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
      </div>
    </form>
</template>

<script>
export default {
  data: function() {
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
