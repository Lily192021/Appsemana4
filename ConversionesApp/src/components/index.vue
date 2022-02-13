<template class="generalTemplate" lang="html">

  <section class="src-components-index">
    
      <!--Agregar titulo-->
    <section class="divIcon">
   <p class="h1 mb-2">Medidas de conversion <b-icon icon="calculator-fill"></b-icon></p>
   </section>
      <!--Implementacion de la primera pagina-->
      <div class="page1Lengths">
        <Page1/>
        
        </div>
        <!--Implementacion de la segunda pagina-->
        <div class="page2Lengths">
          <Page2/>
          </div>
          <!--Implementacion de la tercera pagina-->
          <div class="page3">
              <Page3/>
            </div>
            <!--Implementacion de la cuarta pagina-->
            <div class="page4">
              <Page4/>
              </div>
              <!--Implementacion de la quinta pagina-->
              <div class="page5">
              <Page5/>
              </div>
  </section>
 
</template>

<script lang="js">
import Page1 from './pageLengths.vue';
import Page2 from './pageLengths1.vue';
import Page3 from './pageLengths2.vue';
import Page4 from './pageLengths3.vue';
import Page5 from './pageLengths4.vue';


  export default  {
    name: 'src-components-index',
    components:{
      Page1,
      Page2,
      Page3,
      Page4,
      Page5

    },
    props: [],
    mounted () {

    },
    data () {
      return {

      }
    },
    methods: {

    },
    computed: {

    }
}


</script>

<style scoped lang="scss">
.src-components-index {
  color: black;
}
.divIcon {
  color: white;
  margin: 0;
  padding: 10px;
}

</style>
