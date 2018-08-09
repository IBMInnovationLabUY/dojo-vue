<template>
	<div @click="number = 0" class="prueba" title="Click para resetear"><h1>Hola {{ name }}</h1> <p :style="style">{{ otro }} Desde hace {{ number }} segundos estás en esta página </p></div>
</template>
<script>
export default {
  name: 'Hello',
  data () {
	 return { number: 1, name: "usuario", otro:" IBM Cloud - " }
    },
    created(){
  				setInterval(() => {
  				this.number++;
  			  }, 1000);
  	},
    mounted(){
      this.name = prompt("Ingrese su nombre:")
    },
    computed: {
      style() {
        return {color: this.alert ? 'red' : 'green',fontSize:  this.alert ? 20 : 15, backgroundColor: this.alert ? 'yellow' : 'black'}
      },
  	  alert(){
  		  return  this.number > 20 ? true : false;
  	   }
    }
}
</script>

<style>
.prueba{
font-family:cursive;
}
</style>
