<template>
  <div id="app">
    <car-info 
      v-for="car in cars"
      :key="car.id"
      :make="car.make"
      :model="car.model"
      :year="car.year"
      :owner-name="car.ownerName"
    />
  </div>
</template>

<script>
import CarInfo from './components/CarInfo.vue'

export default {
  name: 'App',
  components: {
    CarInfo
  },
  data() {
    return {
      cars: [
        {
          id: 1,
          make: "Tesla",
          model: "Model 3",
          year: 2021,
          ownerName: "John Doe",
        },
        {
          id: 2,
          make: "Ford",
          model: "F-150",
          year: 2010,
          ownerName: "Jane Doe",
        },
        {
          id: 3,
          make: "Toyota",
          model: "Land Cruiser",
          year: 2020,
          ownerName: "James Doe"
        },
      ],
    }
  },
}
</script>
