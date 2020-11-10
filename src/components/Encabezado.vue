<template>
 <div id="header" :style="{'background-color': getBackGroundFromPrincipal}">

		<h4>The Great <br>
			<span id="colorDisplay">rgb({{colorJugar.r}}, {{colorJugar.g}}, {{colorJugar.b}})</span>
			<br>
            Guessing Game
        </h4>
	</div>

</template>

<script>

  export default  {
    name: 'Encabezado',
    props: ['colorJugar', 'gano'],
    mounted () {

    },
    data () {
      return {
      }
    },
    methods: {

    },
    computed: {
      
      getBackGroundFromPrincipal(){
        const backgroundColor = `rgb(${this.colorJugar.r},${this.colorJugar.g},${this.colorJugar.b})`;
        let value;
        if (this.gano) {
          value= backgroundColor;
        } else {
          value= "rgb(34, 80, 139)";
        }
          return value;
        }
    }
}


</script>

<style scoped lang="css">
  h1 {
  font-weight: normal;
  line-height: 1.1;
  padding: 20px 0;
}
#colorDisplay {
  font-size: 200%;
}
#header {
	background: steelblue;
	text-transform: uppercase;
	text-align: center;
	margin: 0;
	color: white;
}
</style>
