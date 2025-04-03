<script>
export default {
  props: ['car'],

  emits: ['car-deleted', 'car-edited'],
}
</script>

<template>
  <li>
    <span> {{ car }} &nbsp;</span>
    <input :value="car" @change="$emit('car-edited', $event.target.value)" />
    <button>📝</button>
    <button @click="$emit('car-deleted', car)">Удалить</button>
  </li>
</template>
