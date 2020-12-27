<script lang="ts">
import Component, { mixins } from 'vue-class-component';
import DefaultNumber from '../mixins/defaultNumber';
 @Component
export default class CounterByTen extends  mixins(DefaultNumber) {
 increase() {
    this.valueNumber += 10;
  }
 decrease() {
    this.valueNumber -= 10;
  }
}
</script>

<template>
  <div>
    <fieldset>
      <legend>{{ this.formattedNumber }}</legend>
        <button @click="increase">Incrementa en diez</button>
        <button @click="decrease">Decrementa en diez</button>
    </fieldset>
  </div>
</template>