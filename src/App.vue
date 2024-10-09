<template>
<!-- html goes here -->
  <h1>naše první vue appka</h1>
  <div>{{ 2 + 2 }}</div>
  <!-- interpolace -->
  <div>{{ 5 > 3 }}</div>
  <div>{{ firstname + ' ' + lastname }}</div>
  <div>{{ 'his first dog\'s name is ' + dogs[0].name }}</div>
  <TButton label="tlačítko" />
  <TButton label="click me" />
  <TButton label="OK" />
  <TButton label="10+2" />


  <TButton :label="10 + 2"/>
  <!-- direktiva v-bind  -->
  <TButton :label="firstname" />
  <TButton label="firstname" />
  <TButton :label="dogs[0].name + ' is ' + dogs[0].breed" />
  <div>
    <input :disabled="isDisabled">
  </div>

</template>


<script>
// javascript goes here
// importovat a registrovat dceřinnou komponentu

import TButton from '@/components/TButton.vue'


export default {
  name: 'App',
  // data musí být funkce/metoda, která vrací objekt
  data () {
    return {
      firstname: 'Karel',
      lastname: 'Houska',
      dogs: [
        {
          name: 'Alík',
          breed: 'cocker'
        }
      ],
      isDisabled: false
    }
  },
  components: { TButton: TButton }
}

</script>


<style scoped>
/* css goes here */


</style>