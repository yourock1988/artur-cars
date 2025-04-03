<script>
export default {
  props: ['carsCounter'],
}
</script>

<template>
  <div>
    <h3>
      <span>Всего машин: </span>
      <i>{{ carsCounter }}</i>
    </h3>
  </div>
</template>
