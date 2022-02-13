<template lang="html">
  <section class="src-components-prueba">
    <h1> {{msg}}</h1>
  </section>

</template>

<script lang="js">

  export default  {
    name: 'src-components-prueba',
    props: [],
    mounted () {

    },
    data () {
      return {
        msg:'Hola esto es una prueba' 

      }
    },
    methods: {

    },
    computed: {

    }
}


</script>

<style scoped lang="scss">
  .src-components-prueba {
        color: white;
  }
  .h1{
        color:violet;
  }
</style>
