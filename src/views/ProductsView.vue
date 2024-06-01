<template lang="">
  <section class="container">
  <div>
    <h1 class="text-center">Productos</h1>
  </div>
  <div class="row">
      <div class="col-sm-4 col-12 px-5 mb-4">
        <div class="card">
          <img src="../assets/img/colaciones.jpg" class="card-img-top" alt="colaciones" />
          <div class="card-body">
            <h5 class="card-title fw-bold">{{nombre}}</h5>
            <p class="card-text">
              {{descripcion}}
            </p>
          </div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item">{{ formatPrice(precio) }}</li>
            <li class="list-group-item">{{cantidad}}</li>
          </ul>
          <div class="card-body">
            <a href="#" class="card-link">Ver más</a>
            <a href="#" class="card-link">Comprar</a>
          </div>
        </div>
      </div>
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
  props: {
    nombre: {
      type: String,
      required: true
    },
    descripcion: {
      type: String,
      required: true
    },
    precio: {
      type: Number,
      required: true
    },
    cantidad: {
      type: String,
      required: true
    },
  },
  methods: {
    volverInicio() {
      return this.$router.push('/')
    },
    formatPrice(value) {
      return new Intl.NumberFormat('es-CL', {
        style: 'currency',
        currency: 'CLP'
      }).format(value);
    }
  }
}
</script>
<style></style>