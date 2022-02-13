<template lang="html">

  <section class="src-components-page-lengths-4">
     <b-card bg-variant="dark">
    <b-form-group
      label-cols-lg="3"
      label="Conversor de Almacenamiento"
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
        <b-form-input v-model="data5" type="number" id="n1"></b-form-input>
      </b-form-group>
      <b-form-group
        label="Conversion a:"
        label-cols-sm="3"
        label-align-sm="right"
        class="mb-0">
        <b-form-select v-model="selected5">
          
          <b-form-select-option :value="null">Por favor seleccione una opcion</b-form-select-option>
          <b-form-select-option   value="a">Bit a Byte</b-form-select-option>
           <b-form-select-option id="opB"  value="b">Bit a Nibble</b-form-select-option>
            <b-form-select-option id="opC"  value="c">Exabit a Exabyte</b-form-select-option>
             <b-form-select-option id="opD"  value="d">Megabyte a Megabit</b-form-select-option>
              <b-form-select-option id="opE"  value="e">Megabyte a Gigabit</b-form-select-option>
              
        </b-form-select>
        <hr>
        <b-button @click="calcular5" variant="info" size="lg" class="pt-2">Convertir a</b-button>
    </b-form-group>
    </b-form-group>
  </b-card>
  </section>

</template>

<script lang="js">

  export default  {
    name: 'src-components-page-lengths-4',
    props: [],
    mounted () {

    },
    data () {
      return {
        selected5: null,
        data5: ''

      }
    },
    methods: {
        calcular5() {
          let comparador5 = this.selected5
          if (comparador5 == 'a')
          {
            var Bit = this.data5;
            var Byte = 0.13;
            var Operacion1E = (Bit*Byte);
            alert('El resultado es: ' + Operacion1E);
          }
         else if (comparador5 == 'b')
          {
            var Bit1 = this.data5;
            var Nibble = 0.13;
            var Operacion2E = (Bit1*Nibble);
            alert('El resultado es: ' + Operacion2E);
          }
         else if (comparador5 == 'c')
          {
            var ExaBit = this.data5;
            var ExaByte = 0.13;
            var Operacion3E = (ExaBit*ExaByte);
            alert('El resultado es: ' + Operacion3E);
          }
         else if (comparador5 == 'd')
          {
            var Megabyte1 = this.data5;
            var Megabit1 = 8;
            var Operacion4E = (Megabyte1*Megabit1);
            alert('El resultado es: ' + Operacion4E);
          }
         else if (comparador5 == 'e')
          {
            var Megabyte2 = this.data5;
            var GigaBit = 0.01;
            var Operacion5E = (Megabyte2*GigaBit);
            alert('El resultado es: ' + Operacion5E);
          }
          else 
          {
            alert('Por favor seleccione una opcion')
          }

          
        }
    },
    computed: {

    }
}


</script>

<style scoped lang="scss">
  .src-components-page-lengths-4 {
      color: white
  }
</style>
