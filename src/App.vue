<template>
  <div id="app">
    <Contador/>
    <hr />
    <ContadorEnDiez />
    </div>
</template>
 <script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
import Contador from './components/Contador.vue';
import ContadorEnDiez from './components/CounterByTen.vue';
 @Component({
  components: {
    Contador,
    ContadorEnDiez
  },
})
export default class App extends Vue {}
</script>
<style lang="stylus">
  #app
    font-family 'Avenir', Helvetica, Arial, sans-serif
    -webkit-font-smoothing antialiased
    -moz-osx-font-smoothing grayscale
    text-align center
    color #2c3e50
    margin-top 60px
</style>