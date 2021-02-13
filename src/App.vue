<template>
  <div id="app">
    <car-info 
      make="Tesla" 
      model="Model3" 
      year="2021" 
      owner-name="Elon Musk" 
    />
  </div>
</template>

<script>
import CarInfo from './components/CarInfo.vue'

export default {
  name: 'App',
  components: {
    CarInfo
  }
}
</script>
