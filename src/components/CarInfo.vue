<template>
  <div class="car-info" v-on:click="clickHandler">
    <h1>
      This car is a {{ make }} {{ mutatedModel }}, 
      made in {{ year }}, 
      owned by {{ ownerName }}
    </h1>
  </div>
</template>

<script>
export default {
  name: 'CarInfo',
  props: {
    make: String,
    model: String,
    year: String,
    ownerName: String,
  },
  data() {
      return {
          mutatedModel: this.model,
      }
  },
  methods: {
    clickHandler() {
        this.mutatedModel = "Model S"
    }
  },
}
</script>