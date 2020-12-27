<template>
  <div>
    <fieldset>
      <legend>{{ this.formattedNumber }}</legend>
      <button @click="increase">Incremebnta en uno</button>
      <button @click="decrease">Decrementa en uno</button>
    </fieldset>
</div>
</template>
 <script lang="ts">
import Component, { mixins } from 'vue-class-component';
import DefaultNumber from '../mixins/defaultNumber';
 @Component
export default class Contador extends mixins(DefaultNumber) {
  increase() {
    this.valueNumber += 1;
  }
 decrease() {
    this.valueNumber -= 1;
  }
}
</script>

<!--<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
 @Component
export default class Contador extends Vue {
  valueNumber: number = 0;
 get formattedNumber() {
    return `El valor total es:  ${this.valueNumber}`;
  }
increase() {
    this.valueNumber += 1;
  }
 decrease() {
    this.valueNumber -= 1;
  }
}
</script>
<template>
  <div>
    <fieldset>
      <legend>{{ formattedNumber }}</legend>
        <button @click="increase">Increase</button>
        <button @click="decrease">Decrease</button>
    </fieldset>
  </div>
</template>-->