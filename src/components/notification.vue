<template>
    <div class="container" v-show="clos">
      <div class="close" @click="shutDown">
        <img class="min cls" src="../assets/close.svg" alt="">
      </div>
      <div class="content">
        <h3>Show Notifications</h3>
      <div class="sub">
        <img class="min bell" src="../assets/bell-notification-svgrepo-com.svg" alt="">
        <p>www.freecodecamp.org</p>
      </div>
      </div>

    </div>
</template>

<script setup>
import {ref} from 'vue'

const clos= ref(true)

const shutDown = ()=> {
    clos.value = !clos.value
}

const emits = defineEmits(["close"])

function clickHandler(){
    emits("close")
}

</script>

<style>
.container{
    background-color: rgb(100, 136, 124);
    width: 500px;
    height: 170px;
    position: absolute;
    bottom: 230px;
    left: 100px;
    border-radius: 15px;
}
.min{
    width: 40px;
}

.bell{
    position: absolute;
    top: 60px;
    left: 120px;
}
.cls{
    position: absolute;
    top: 5px;
    right: 5px;
    cursor: pointer;

}
.cls:hover{
    width: 43px;
}
.content h3{
    position: absolute;
    top: 4px;
    left: 170px;
}
.sub p{
    position: absolute;
    top: 55px;
    left: 170px; 
    color: #fff;
}
</style>