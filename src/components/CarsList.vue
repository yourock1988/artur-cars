<script>
import CarItem from './CarItem.vue'

export default {
  components: { CarItem },

  props: ['modelValue'],

  emits: ['update:model-value'],
}
</script>

<template>
  <ul>
    <CarItem
      v-for="(car, idx) of modelValue"
      :key="idx"
      :car="car"
      @car-edited="
        $emit(
          'update:model-value',
          modelValue.map(c => (c === car ? $event : c))
        )
      "
      @car-deleted="
        $emit(
          'update:model-value',
          modelValue.filter(c => c !== car)
        )
      "
    />
  </ul>
</template>
