<script>
import CarAdder from './components/CarAdder.vue'
import CarsList from './components/CarsList.vue'

export default {
  components: { CarAdder, CarsList },

  data() {
    return {
      cars: ['Mercedes', 'BMW', 'Audi'],
    }
  },
}
</script>

<template>
  <div>
    <CarAdder @car-added="cars.push($event)" />

    <CarsList :cars="cars" @car-deleted="cars = $event" />

    <button>Очистить ВСЁ</button>
  </div>
</template>
