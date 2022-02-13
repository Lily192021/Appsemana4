<template lang="html">

  <section class="src-components-page-lengths-3">
    <b-card bg-variant="success">
    <b-form-group
      label-cols-lg="3"
      label="Conversor de tiempo"
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
        <b-form-input v-model="data4" type="number" id="n1"></b-form-input>
      </b-form-group>
      <b-form-group
        label="Conversion a:"
        label-cols-sm="3"
        label-align-sm="right"
        class="mb-0">
        <b-form-select v-model="selected4">
          
          <b-form-select-option :value="null">Por favor seleccione una opcion</b-form-select-option>
          <b-form-select-option   value="a">Minutos a Horas</b-form-select-option>
           <b-form-select-option id="opB"  value="b">Minutos a Dias</b-form-select-option>
            <b-form-select-option id="opC"  value="c">Decadas a Siglos</b-form-select-option>
             <b-form-select-option id="opD"  value="d">Horas a años</b-form-select-option>
              <b-form-select-option id="opE"  value="e">Meses en años</b-form-select-option>
              
        </b-form-select>
        <hr>
        <b-button @click="calcular4" variant="dark" size="lg" class="pt-2">Convertir a</b-button>
    </b-form-group>
    </b-form-group>
  </b-card>
  </section>

</template>

<script lang="js">

  export default  {
    name: 'src-components-page-lengths-3',
    props: [],
    mounted () {

    },
    data () {
      return {
        selected4: null,
        data4: ''

      }
    },
    methods: {
      calcular4() {
       let comparador4 = this.selected4
       if (comparador4=='a')
       {
         var m = this.data4;
         var h = 0.01667;
         var operacion1D = (m*h);
         alert('El resultado es: ' + operacion1D);
       }
      else if (comparador4=='b')
       {
         var m1 = this.data4;
         var d = 0.00069458333;
         var operacion2D = (m1*d);
         alert('El resultado es: ' + operacion2D);
       }
      else if (comparador4=='c')
       {
         var decadas = this.data4;
         var siglos = 0.10001999952;
         var operacion3D = (decadas*siglos);
         alert('El resultado es: ' + operacion3D);
       }
       else if (comparador4=='d')
       {
         var horas = this.data4;
         var years = 0.00011410236797843;
         var operacion4D = (horas*years);
         alert('El resultado es: ' + operacion4D);
       }
       else if (comparador4=='e')
       {
         var meses = this.data4;
         var years1 = 0.0833499996;
         var operacion5D = (meses*years1);
         alert('El resultado es: ' + operacion5D);
       }
       else{
         alert('Seleccione una opcion por favor!')
       }

      }

    },
    computed: {

    }
}


</script>

<style scoped lang="scss">
  .src-components-page-lengths-3 {
    color: white;

  }
</style>
