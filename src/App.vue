<template>
  <div>
    <NavPart></NavPart>
    <GridPart></GridPart>
    <FormPart></FormPart>
    <TwocolPart></TwocolPart>
    <FooterPart></FooterPart>
  </div>

</template>




<script>
import NavPart from './components/NavPart.vue'
import GridPart from './components/GridPart.vue'
import FormPart from './components/FormPart.vue'
import TwocolPart from './components/TwocolPart.vue'
import FooterPart from './components/FooterPart.vue'


export default{
  name: 'App',

  data(){
    return{
      showModal : false
    }
  },

  components: {
    NavPart,
    GridPart,
    FormPart,
    TwocolPart,
    FooterPart,
  },

  methods: {
    closeBox(){
      console.log("ksdjf")
    }
  }
}
</script>

<style>

</style>
