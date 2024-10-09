<template>
  <button>{{ label }}</button>
</template>

<script>

export default {
  name: 'TButton',
  data () {
    return {
      label2: '...'
    }
  },
  // props: {
  //   label: {
  //     type: String,
  //     default: 'Ahoj',
  //     validator: (v) => v.length >= 2
  //   }
  // }
  props: ['label']
}

// definice props
  // 1)  pole s názvy props jako stringy
  // 2) objekt se strukturou prop: DatovýTyp
  // 3) objekt se strukturou prop: { konfigurace }

</script>

<style scoped>
  button {
    padding: .35em .7em;
    font-size: 1.2rem;
    border: 1px solid #909090;
    background: white;
    cursor: pointer;
    display: block;
  }
  button:hover {
    background: lightpink;
  }
</style>