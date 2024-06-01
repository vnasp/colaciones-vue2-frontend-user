<template>
  <Navbar />
  
  <router-view/>
  
  <medios-pago/>
  <Footer />
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Footer from '@/components/Footer.vue'
import MediosPago from '@/components/MediosPago.vue'

export default {
  name: 'HomeView',
  components: {
    Navbar,
    Footer,
    MediosPago
  }
}
</script>
<style>
.button{
  margin-top:10px;
  padding:5px;
  color: white;
  background-color:rgb(232, 62, 140);
}
</style>