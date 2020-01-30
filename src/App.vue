<template>
  <div id="app">
    <h1>hola vue</h1>
    <table style="width:100%">
  <tr v-for="radiobase in radiobases" :key="id">
    <th>{{radiobase}}</th>
  </tr>
  

    
    

  <!-- <tr >
    <td v-for="radiobase in radiobases" :key="radio">
     {{radiobase.radio1}}
    </td>
  </tr> -->
  
</table>
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
      radiobases: [],
      elementos: [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30]
    }
  },
  mounted(){
    axios.get('http://localhost:4000/telcel')
    .then(res => {
      console.log('res',res)
      this.radiobases = res.data
      console.log('radiobases', this.radiobases)
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
</style>
