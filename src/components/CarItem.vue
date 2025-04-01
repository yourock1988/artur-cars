<script>
export default {
  props: ['car'],

  emits: ['car-deleted'],
}
</script>

<template>
  <li>
    <span> {{ car }} &nbsp;</span>
    <button @click="$emit('car-deleted', car)">Удалить</button>
  </li>
</template>
