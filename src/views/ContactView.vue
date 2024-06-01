<template lang="">
  <section>
  <div>
    <h1 class="text-center">Contacto</h1>
  </div>
  <BackToHome/>
  </section>
</template>
<script>
import BackToHome from './../components/BackToHome.vue'

export default {
  components: {
    BackToHome
  },
  methods: {
    volverInicio() {
      return this.$router.push('/')
    }
  }
}
</script>
<style>
</style>