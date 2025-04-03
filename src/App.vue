<script>
import CarAdder from './components/CarAdder.vue'
import CarsList from './components/CarsList.vue'
import CarsCounter from './components/CarsCounter.vue'

export default {
  components: { CarAdder, CarsList, CarsCounter },

  data() {
    return {
      cars: ['Mercedes', 'BMW', 'Audi'],
    }
  },
}
</script>

<template>
  <div>
    <CarsCounter :cars-counter="cars.length" />

    <CarAdder @car-added="cars.push($event)" />

    <CarsList v-model="cars" />

    <button @click="cars = []">Очистить ВСЁ</button>

    <!-- <CarsList :cars="cars" @update-cars="cars = $event" /> -->

    <!-- <CarsList :model-value="cars" @update:model-value="cars = $event" /> -->
  </div>
</template>
