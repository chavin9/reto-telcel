<template>
  <div id="app">
    <h1>hola vue</h1>
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
        {{trafico}}
      </ul>
      </div>
    </div>
  <!-- <tr v-for="radiobase in radiobases" :key="id" >
  </tr>
  <tr v-for="elemento in elementos1" :key="id">
      {{elemento}}
    </tr> -->
   
    <!-- <t> {{elemento.FECHA}}</tr>
    <td>{{elemento.TRAFICO}} </td> -->
  
  
  

    
    

  <!-- <tr >
    <td v-for="radiobase in radiobases" :key="radio">
     {{radiobase.radio1}}
    </td>
  </tr> -->
  
<!-- </table> -->
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      esMenor0_15: null,
      esMenor15_40: null,
      esMenor40_90: null,
      mayor_90: null,
      traficos1:[],
      
    }
  },
  mounted(){
    axios.get('http://localhost:4001/telcel')
    .then(res => {
      console.log('res',res)
      this.radiobases = res.data[0]
      this.traficos1 = res.data[1][0]
      console.log('elementos1',this.traficos1)
      
      //console.log(this.elementos)
    })
  },

  
  
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

.mayor-15{
  background-color: red;
}

.tabla{
  display: flex;
  flex-direction: row;

}
</style>
