<template>
<h1> لیست کارهای روزانه </h1>
  <div>
    <h1> لیست کارهای روزانه </h1>
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1420 320">
    <path fill="#F3F4F5" fill-opacity="1" d="M0,128L48,144C96,160,192,192,288,181.3C384,171,480,117,576,96C672,75,768,85,864,106.7C960,128,1056,160,1152,160C1248,160,1344,128,1392,112L1440,96L1440,0L1392,0C1344,0,1248,0,1152,0C1056,0,960,0,864,0C768,0,672,0,576,0C480,0,384,0,288,0C192,0,96,0,48,0L0,0Z">
    </path>

    </svg>
      <img src="./assets/19830-removebg-preview.png">
      <div class="div-input">
        <buttonadd @click="addtodo" textbtn="افزودن" />
        <textinput v-model="content" />
        <myapp :removetodo="removetodo" :items="items" />
      </div>
  </div>
</template>

<script>
import myapp from './components/myapp.vue'
import buttonadd from './components/buttonadd.vue'
 import textinput from './components/textinput.vue'

export default {
  name: 'App',
  components: {
     myapp,
    buttonadd,
    textinput
  },
  data(){
    return{
      textin:'',
      content:'',
      text:'کارهاتو اینجا بنویس ...',
      items:[]
    }
  },
  methods:{

    addtodo :function(){
    if(this.content==""){
        console.log('enter value!')
    }
    else {
      console.log(this.content)
    this.items.push(this.content)
    this.content=''
    }
    
},
removetodo : function(index){
    this.items.splice(index,1)
},
add(UserDate){
  this.title=UserDate
}

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0;
  direction: rtl;
  font-family: IS;
}
svg{
  height: 600px;
  position: relative;
}
img{
  width: 600px;
  z-index: 555;
  float: right;
  margin-top: -567px !important;
  position: relative;
    }
        @media(min-width:380px){
      .div-input{
        margin:-169px auto !important ;
      }
    }

    @media(min-width:1000px){
      .div-input{
            margin: -409px 551px !important;
      }
    }
    @media( min-width:1200px){
      .div-input{
            margin: -409px 678px !important;
      }
    }
    @media(max-width:1000px){
      img{
        margin: -569px auto !important;
        position: relative;
      }
      .div-input{
        margin: -50px auto !important;
      }
    }
    @media(max-width:500px){
      .div-input{
        margin:-160px auto !important ;
        width:100% ;
        padding: 24px 0;
      }
      img{
        width: 100%;
      }
    }
    /* @media(max-width:470px){
      .div-input{
        margin:-150px auto !important ;
      }
    } */
    @media(max-width:400px){
      .div-input{
        margin:-230px auto !important ;
        padding: 24px 0;
      }

    }
    h1{
      position: relative;
      margin-top: -85px;
    }
</style>
