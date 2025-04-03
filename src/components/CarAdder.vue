<script>
export default {
  emits: ['car-added'],

  data() {
    return {
      car: '',
    }
  },

  methods: {
    handleClick(e) {
      if (this.car === '') return
      this.$emit('car-added', this.car)
      this.car = ''
      this.$refs.elInput.focus()
    },
  },
}
</script>

<template>
  <div>
    <input ref="elInput" v-model="car" />

    <button @click="handleClick">Добавить</button>
  </div>
</template>
