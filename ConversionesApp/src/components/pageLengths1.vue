<template lang="html">

  <section class="src-components-page-lengths-1">
    <b-card bg-variant="warning">
    <b-form-group
      label-cols-lg="3"
      label="Conversor de monedas"
      label-size="lg"
      label-class="font-weight-bold pt-0"
      class="mb-0"
    >
      <b-form-group
        label="Primer Valor:"
        label-for="n1"
        label-cols-sm="3"
        label-align-sm="right"
      >
        <b-form-input v-model="data2" type="number" id="n1"></b-form-input>
      </b-form-group>
      <b-form-group
        label="Conversion a:"
        label-cols-sm="3"
        label-align-sm="right"
        class="mb-0">
        <b-form-select v-model="selected1">
          
          <b-form-select-option :value="null">Por favor seleccione una opcion</b-form-select-option>
          <b-form-select-option   value="a">Dolar a Euro</b-form-select-option>
           <b-form-select-option id="opB"  value="b">Euro a Dolar</b-form-select-option>
            <b-form-select-option id="opC"  value="c">Colon a Dolar</b-form-select-option>
             <b-form-select-option id="opD"  value="d">Dolar a Colon</b-form-select-option>
              <b-form-select-option id="opE"  value="e">Libra Esterlina a Dolar</b-form-select-option>
              
        </b-form-select>
        <hr>
        <b-button @click="calcular2" variant="dark" size="lg" class="pt-2">Convertir a</b-button>
    </b-form-group>
    </b-form-group>
  </b-card>
  </section>

</template>

<script lang="js">

  export default  {
    name: 'src-components-page-lengths-1',
    props: [],
    mounted () {

    },
    data () {
      return {
        selected1: null,
        data2:''

      }
    },
    methods: {
      calcular2(){
       
      var comparar = this.selected1;
     
      
      console.log(comparar);
      if (comparar == 'a')
      {
        var dolar = this.data2;
        var euro = 0.8252;
        var operacionB = (dolar * euro).toFixed(2);
        alert('El resultado fue: '+ operacionB)
        
      }
       else if (comparar == 'b')  
      {
        var euro1 = this.data2;
        var dolar1 = 1.2118;
        var operacion1B = (euro1*dolar1).toFixed(2); 
        alert('El resultado es: ' + operacion1B)
      }
      else if (comparar == 'c')
      {
        var colon = this.data2;
        var dolar2 = 0.1141;
        var operacion2B = (colon*dolar2).toFixed(2);
        alert('El resultado es: ' + operacion2B)
      }
      else if (comparar == 'd')
      {
          var dolar3 = this.data2;
          var colon1 = 8.7653;
          var operacion3B = (dolar3*colon1).toFixed(2);
          alert('El resultado es: ' + operacion3B) 
      }
      else if (comparar == 'e')
      {
          var dolar4 = this.data2;
          var libra = 1.4016;
          var operacion4B = (dolar4*libra).toFixed(2);
          alert('El resultado es: ' + operacion4B) 
      }
      else 
      {
        alert('Seleccione una opcion por favor!')
      }
       

      }

    },
    computed: {

    }
}


</script>

<style scoped lang="scss">
  .src-components-page-lengths-1 {
    color: black;

  }
</style>
