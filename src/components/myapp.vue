<template>        
<h1 class="title"> لیست کارهای روزانه </h1>
    <div class="box-todo">
        <table>
            <tbody>
                <tr v-for='(item,index) in items' :key="item">
                    <counter :index="index"/>
                    <list-item :item="item" />
                    <deletebtn @click="removetodo(index)" />
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
import Counter from './counter.vue'
import deletebtn from './deletebtn.vue'
import ListItem from './list-item.vue'
export default {
  components: { deletebtn, Counter, ListItem },
    name:'myapp',
    props:{
        items:Array,
        removetodo:Function,
    },
    data(){
        return{
        }
    }

}
</script>

<style>
    @font-face{
        font-family: IS;
        font-size: normal;
        src: url("../font/IRAN Sans Regular (mmrostami.blog.ir).ttf");
    }
    
    .title{
        margin-top: -170px;
    }
    body{
        background-color: #f88f2d;
        
    }
    table{
        display: block !important;
        margin-top: 156px;
    }
    tbody{
        display: block;
        margin: 0 auto !important;
    }
    tr td{
        position: relative;
        z-index: 555;
        margin: 10px auto !important;
        font-size: 18px;
    }
    tr{
        display: flex;
        margin: 20px auto;
        border-bottom: 1px solid #cacaca;
    }
    i{
        cursor: pointer;
        color: red;
    }
    input{
        padding: 12px;
        border: none;
        border-bottom: 1px solid #f78e06;
        outline: none;
        font-family: IS;
        background: transparent;
    }
    ::placeholder{
        font-size: 18px;
    }
    #send{
        cursor: pointer;
        padding: 8px 15px;
        border: none;
        outline: none;
        font-family: IS;
        font-size: 18px;
        background-color: #f88f2d;
        border-radius: 5px;
        backdrop-filter: blur( 8px );
        -webkit-backdrop-filter: blur( 4px );
    }
    .div-input{
    width: 400px;
    padding: 20px;
    margin: -409px 706px !important;
    z-index: 555;
    position: relative;
    background: rgba( 255, 255, 255, 0.55); 
    box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
    backdrop-filter: blur( 8px );
    -webkit-backdrop-filter: blur( 4px );
    border: 1px solid rgba( 255, 255, 255, 0.18 );
     border-radius: 34px;
        }

</style>