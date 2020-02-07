<template>

  <div id="app">
    <h1>Examen Telcel</h1>
    <div class="tabla">
      <div></div>
      <div>
         <h2 style="padding-left: 40px;padding-top: 11px;">Radiobases</h2>
      <ul v-for="radiobase in radiobases" :key="id" >
      
            {{radiobase}}
      </ul>
      </div>
      <div>
         <h4 style="padding-left: 40px;">23 de Agosto</h4>
      <ul v-for="trafico in traficos1" :key="id" >
        <span  v-if="trafico.FECHA == '8/23/2019' " >
          <div :class="{'rojo' : (trafico.TRAFICO <= 15),
                        'naranja': (trafico.TRAFICO > 15 && trafico.TRAFICO <= 40),
                         'amarillo': (trafico.TRAFICO > 40 && trafico.TRAFICO <= 90),
                         'verde': (trafico.TRAFICO > 90 ),
                         'gris': (trafico.TRAFICO === 0),
                         }"> 
                        {{trafico.TRAFICO}}
          </div>
        </span>
      </ul>
      </div>
      <div>
         <h4 style="padding-left: 40px;" >25 de Agosto</h4>
      <ul v-for="trafico in traficos1" :key="id" >
        <span  v-if="trafico.FECHA ==  '8/25/2019'  " >
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
         <h4 style="padding-left: 40px;" >27 de Agosto</h4>
      <ul v-for="trafico in traficos1" :key="id" >
        <span  v-if="trafico.FECHA == '8/27/2019'" >
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
         <h4 style="padding-left: 40px;" >29 de Agosto</h4>
      <ul v-for="trafico in traficos1" :key="id" >
        <span  v-if="trafico.FECHA == '8/29/2019'" >
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
         <h4 style="padding-left: 40px;" >1 de Septiembre</h4>
      <ul v-for="trafico in traficos1" :key="id" >
        <span  v-if="trafico.FECHA == '9/1/2019'" >
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
         <h4 style="padding-left: 40px;" >3 de Septiembre</h4>
      <ul v-for="trafico in traficos1" :key="id" >
        <span  v-if="trafico.FECHA == '9/3/2019' " >
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
         <h4 style="padding-left: 40px;" >4 de Septiembre</h4>
      <ul v-for="trafico in traficos1" :key="id" >
        <span  v-if="trafico.FECHA == '9/4/2019' " >
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
         <h4 style="padding-left: 40px;" >7 de Septiembre</h4>
      <ul v-for="trafico in traficos1" :key="id" >
        <span  v-if="trafico.FECHA == '9/7/2019'" >
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
         <h4 style="padding-left: 40px;" >8 de Septiembre</h4>
      <ul v-for="trafico in traficos1" :key="id" >
        <span  v-if="trafico.FECHA == '9/8/2019'" >
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
         <h4 style="padding-left: 40px;" >9 de Septiembre</h4>
      <ul v-for="trafico in traficos1" :key="id" >
        <span  v-if="trafico.FECHA == '9/9/2019'">
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
      
      traficos1:null,

      radiobases:[],
      
      
    }
  },
  mounted(){
    axios.get('http://localhost:4002/telcel')
    .then(res => {
      console.log('res',res)
      this.radiobases = res.data[1]
      this.traficos1 = res.data[0]
      
     // console.log('Trafico',this.traficos1)
      
      
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

#h4{
  text-align: center;
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
