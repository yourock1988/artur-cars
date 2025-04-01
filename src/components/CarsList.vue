<script>
import CarItem from './CarItem.vue'

export default {
  components: { CarItem },

  props: ['cars'],

  emits: ['car-deleted'],
}
</script>

<template>
  <ul>
    <CarItem
      v-for="(car, idx) of cars"
      :key="idx"
      :car="car"
      @car-deleted="
        $emit(
          'car-deleted',
          cars.filter(c => c !== car)
        )
      "
    />
  </ul>
</template>
