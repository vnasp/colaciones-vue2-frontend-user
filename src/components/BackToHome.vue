<template lang="">
  <div class="text-center pb-4">
    <button class="button" @click="volverInicio">Volver al inicio</button>
  </div>
</template>

<script>
export default {
  methods: {
    volverInicio() {
      return this.$router.push('/')
    }
  }
}
</script>
<style>
</style>