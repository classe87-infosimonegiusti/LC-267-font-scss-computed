<script>

  import MyComponent from './components/MyComponent.vue';

  export default {
    data() {
      return {
        arrayDiNumeri: [1,4,2,18,5,233],
        somma: 0
      }
    },
    methods: {
      sommaArray() {
        console.log('La funzione sommaArray è stata invocata!');
        this.somma = 0;
        for (let i = 0; i < this.arrayDiNumeri.length; i ++) {
          this.somma += this.arrayDiNumeri[i];
        }
      }
    },
    created() {
      this.sommaArray();
    },
    computed: {
      sommaComputataArray() {
        console.log('La proprieta sommaComputataArray è stata invocata!');
        let somma = 0;
        for (let i = 0; i < this.arrayDiNumeri.length; i ++) {
          somma += this.arrayDiNumeri[i];
        }
        return somma;
      }
    },
    components: {
      MyComponent
    }

  }

</script>

<template>

  <MyComponent />

  <i class="fa-solid fa-user"></i>

  <hr/>

  <h1>La somma dell'array è {{ somma }}</h1>
  <h2>La somma dell'array è {{ somma }}</h2>
  <h3>La somma dell'array è {{ somma }}</h3>
  <h4>La somma dell'array è {{ somma }}</h4>
  <h5>La somma dell'array è {{ somma }}</h5>

  <hr/>

  <h1>La somma dell'array è {{ sommaComputataArray }}</h1>
  <h2>La somma dell'array è {{ sommaComputataArray }}</h2>
  <h3>La somma dell'array è {{ sommaComputataArray }}</h3>
  <h4>La somma dell'array è {{ sommaComputataArray }}</h4>
  <h5>La somma dell'array è {{ sommaComputataArray }}</h5>
   
</template>

<style lang="scss">

  @use './styles/general.scss' as *;

</style>
