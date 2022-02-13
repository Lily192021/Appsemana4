<template lang="html">

  <section class="src-components-page-lengths-2">
    <b-card bg-variant="info">
    <b-form-group
      label-cols-lg="3"
      label="Conversor de masa"
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
        <b-form-input v-model="data3" type="number" id="n1"></b-form-input>
      </b-form-group>
      <b-form-group
        label="Conversion a:"
        label-cols-sm="3"
        label-align-sm="right"
        class="mb-0">
        <b-form-select v-model="selected3">
          
          <b-form-select-option :value="null">Por favor seleccione una opcion</b-form-select-option>
          <b-form-select-option   value="a">Kilogramo a Miligramo</b-form-select-option>
           <b-form-select-option id="opB"  value="b">Kilogramo a Libra</b-form-select-option>
            <b-form-select-option id="opC"  value="c">Kilogramo a Gramo</b-form-select-option>
             <b-form-select-option id="opD"  value="d">Libra a Kilogramo</b-form-select-option>
              <b-form-select-option id="opE"  value="e">Libra a Gramo</b-form-select-option>
              
        </b-form-select>
        <hr>
        <b-button @click="calcular3" variant="dark" size="lg" class="pt-2">Convertir a</b-button>
    </b-form-group>
    </b-form-group>
  </b-card>
  </section>

</template>

<script lang="js">

  export default  {
    name: 'src-components-page-lengths-2',
    props: [],
    mounted () {

    },
    data () {
      return {
        selected3: null,
        data3: ''

      }
    },
    methods: {
      calcular3(){
        var comparador3 = this.selected3
        if (comparador3 == 'a')
        {
          let kg = this.data3;
          let mg = 1000000;
          let operacionC = (kg*mg);
          alert('El resultado es: ' + operacionC )
        }
         else if (comparador3 == 'b')
        {
          let kg1 = this.data3;
          let lb = 2.20462;
          let operacion1C = (kg1*lb);
          alert('El resultado es: ' + operacion1C )
        }
        else if (comparador3 == 'c')
        {
          let kg2 = this.data3;
          let g = 1000;
          let operacion2C = (kg2*g);
          alert('El resultado es: ' + operacion2C )
        }
        else if (comparador3 == 'd')
        {
          let lb2 = this.data3;
          let kg3 = 0.453592;
          let operacion3C = (lb2*kg3);
          alert('El resultado es: ' + operacion3C )
        }
        else if (comparador3 == 'e')
        {
          let lb3 = this.data3;
          let g2 = 453.592;
          let operacion4C = (lb3*g2);
          alert('El resultado es: ' + operacion4C )
        }
        else {
          alert('Por favor seleccione una opcion');
        }
      }

    },
    computed: {

    }
}


</script>

<style scoped lang="scss">
  .src-components-page-lengths-2 {
    color: white

  }
</style>
