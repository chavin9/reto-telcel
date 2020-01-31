<template>
  <div id="app">
    <div class="tabla">
      <div>
         <h3>radiobases</h3>
      <ul v-for="radiobase in radiobases" :key="id" >
            {{radiobase.RADIOBASE}}
      </ul>
      </div>
      <div>
         <h3>dia1</h3>
      <ul v-for="trafico in traficos1" :key="id" >
        <span  v-if="trafico.FECHA == '2019-08-23'" >
          <div :class="{'rojo' : (trafico.TRAFICO <= 15),
                        'naranja': (trafico.TRAFICO > 15 && trafico.TRAFICO <= 40),
                         'amarillo': (trafico.TRAFICO > 40 && trafico.TRAFICO <= 90),
                         'verde': (trafico.TRAFICO > 90 ),
                         'gris': (trafico.TRAFICO===0),
                         }"> 
                        {{trafico.TRAFICO}}
          </div>
        </span>
      </ul>
      </div>
      <div>
         <h3>dia2</h3>
      <ul v-for="trafico in traficos1" :key="id" >
        <span  v-if="trafico.FECHA == '2019-08-25'" >
          

   <div :class="{'rojo' : (trafico.TRAFICO <= 15),
                        'naranja': (trafico.TRAFICO > 15 && trafico.TRAFICO <= 40),
                         'amarillo': (trafico.TRAFICO > 40 && trafico.TRAFICO <= 90),
                         'verde': (trafico.TRAFICO > 90 ),
                         'gris': (trafico.TRAFICO===0),
                         }"> 
            {{trafico.TRAFICO}}

          </div>



        </span>
      </ul>
      </div>
      <div>
         <h3>dia3</h3>
      <ul v-for="trafico in traficos1" :key="id" >
        <span  v-if="trafico.FECHA == '2019-08-27'" >
            {{trafico.TRAFICO}}
        </span>
      </ul>
      </div>
      <div>
         <h3>dia4</h3>
      <ul v-for="trafico in traficos1" :key="id" >
        <span  v-if="trafico.FECHA == '2019-08-29'" :class="indicador" >
            {{trafico.TRAFICO}}
        </span>
      </ul>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
       isActive: true,
      hasError: false,
      esMenor0_15: null,
      esMenor15_40: null,
      esMenor40_90: null,
      mayor_90: null,
      traficos1:null,
      radiobases:[],
      
      
    }
  },
  mounted(){
    axios.get('http://localhost:4001/telcel')
    .then(res => {
      console.log('res',res)
      this.radiobases = res.data
      this.traficos1 = res.data
      console.log('elementos1',this.traficos1)
      
      //console.log(this.elementos)
    })
  },
  computed: {
  classObject: function () {
    return {
      active: this.isActive && !this.error,
      'text-danger': this.error && this.error.type === 'fatal'
    }
  }
}

  
  
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.mayor15{
  background-color: red;
  color: black;
}

.tabla{
  display: flex;
  flex-direction: row;

}

.rojo{
  background-color: red;
}
.naranja{
  background-color: orange;
}
.amarillo{
  background-color: yellow;
}
.verde{
  background-color: green;

}
.gris{
  background-color: grey;
}



</style>
