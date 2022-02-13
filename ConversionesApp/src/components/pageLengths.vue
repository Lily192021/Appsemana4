<template lang="html">

  <section class="src-components-page-lengths">
    <b-card bg-variant="danger">
    <b-form-group
      label-cols-lg="3"
      label="Medidas de longitud"
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
        <b-form-input v-model="data1" type="number" id="n1"></b-form-input>
      </b-form-group>
      <b-form-group
        label="Conversion a:"
        label-cols-sm="3"
        label-align-sm="right"
        class="mb-0"
      >
        <b-form-select v-model="selected">
          
          <b-form-select-option :value="null">Por favor seleccione una opcion</b-form-select-option>
          <b-form-select-option   value="a">Kilometros a Metros</b-form-select-option>
           <b-form-select-option id="opB"  value="b">Metros a Kilometros</b-form-select-option>
            <b-form-select-option id="opC"  value="c">Metros a Centimetros</b-form-select-option>
             <b-form-select-option id="opD"  value="d">Centimetros a Metros</b-form-select-option>
              <b-form-select-option id="opE"  value="e">Metros a pies</b-form-select-option>
              
        </b-form-select>
        
        <hr>
        <b-button v-on:click="calcular1" variant="dark" size="lg" class="pt-2">Convertir a</b-button>
    </b-form-group>
    </b-form-group>
  </b-card>
  </section>

</template>

<script lang="js">

  export default  {
    name: 'src-components-page-lengths',
    props: [],
    mounted () {

    },
    data () {
      return {
        selected: null,
        data1:''
        
       

        

      }
    },
    methods: {
      calcular1(){
     var referencia = this.selected;
       
        if (referencia == 'a') {
         
          
          var obtenern= this.data1
          var equivalencia = 1000;
          var operacion =  (obtenern * equivalencia) 
          console.log(operacion );
          var res = (operacion + " Metros")
          alert(res);
          
          
         

        }
        else if (referencia == 'b')
        {
          var obtenern1=this.data1
          var equivalencia1 = 1000;
          var operacion1 = (obtenern1 / equivalencia1);
          console.log(operacion1);
          alert(operacion1 + " Kilometros");
         

        }
        else if (referencia == 'c')
        {
          var obtenern2=this.data1
          var equivalencia2 = 100;
          var operacion2 = (obtenern2 * equivalencia2);
          console.log(operacion2);
          alert(operacion2 + " Centimetros");
            
        }
        else if (referencia == 'd')
        {
          var obtenern3=this.data1
          var equivalencia3 = 100;
          var operacion3 = (obtenern3 / equivalencia3);
          console.log(operacion3);
          alert(operacion3 + " Metros");
         

        }
        else if (referencia == 'e')
        {
          var obtenern4=this.data1
          var equivalencia4 = 3.281;
          var operacion4 = (obtenern4 * equivalencia4);
          console.log(operacion4);
          alert(operacion4 + " Centimetros");
          

        }
        else {
          alert('Seleccione una opcion, por favor!')
        }

      }

    },
    computed: {

    }
}


</script>

<style scoped lang="scss">
.src-components-page-lengths {
  color: white;
}
</style>
