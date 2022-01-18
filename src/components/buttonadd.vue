<template>
     <button type="submit" v-on="$Listeners" id="send"> {{textbtn}} </button>
</template>

<script>
export default {
    name:'buttonadd',
    props:['textbtn']
}
</script>

<style>

</style>