<template> 
	<p :style="style">Número: {{ number }}</p>
</template>
<script>
export default {
  name: 'Hello',
  data () {
    name: "",
	number: 1,
	max:10
    },
  computed: {
      style() {
        return {color: this.alert ? 'red' : 'green',fontSize:  this.alert ? 20 : 15, backgroundColor: this.alert ? 'yellow' : 'black'}
      }
    }
}
</script>

<style></style>

