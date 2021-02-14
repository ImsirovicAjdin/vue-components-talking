<template>
  <div class="car-info" v-on:click="sendMessageToParent">
    <h1>
      This car is a {{ make }} {{ model }}, 
      made in {{ year }}, 
      owned by {{ ownerName }}.
    </h1>
    <em v-if="onSale">This car is on sale</em>
  </div>
</template>

<script>
export default {
  name: 'CarInfo',
  props: {
    id: Number,
    make: String,
    model: String,
    year: Number,
    ownerName: String,
    onSale: Boolean,
  },
  methods: {
    sendMessageToParent() {
        this.$emit('custom-event-name', this.id)
    }
  },
}
</script>