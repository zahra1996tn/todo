<template>
    <div>
        <table>
            <tbody>
                <tr v-for='(item,index) in items' :key="item">
                    <td> {{index+1}} </td>
                    <td> {{item}}</td>
                    <td> <i @click="removetodo(index)"> حذف </i> </td>
                   
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
export default {
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
    body{
        background-color: #f88f2d;
        
    }
    table{
        display: block !important;
        margin-top: 50px;
    }
    tbody{
        display: block;
        margin: 0 auto !important;
    }
    tr td{
        /* list-style-type: none; */
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

        /* box-shadow:  33px 33px 66px #cecece,
             -33px -33px 66px #f2f2f2;  */
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
    /* border-radius: 10px; */
    border: 1px solid rgba( 255, 255, 255, 0.18 );
    /* shadow */
     border-radius: 34px;
    /*background: #f0f0f0; */
    /* box-shadow: inset 12px 12px 18px #c7c7c7,
            inset -12px -12px 18px #f9f9f9; */
        }

</style>