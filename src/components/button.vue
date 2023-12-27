<template>
    <div>
        <button class="show" @click="clickHandler">Show</button>
        <button class="block" @click="clickHandler">Block</button>
        <button class="allow" @click="clickHandler">Allow</button>
    </div>
</template>

<script setup>
const emtis = defineEmits(["show","block", "allow"])

function clickHandler(){
    emtis("show")
    emtis("block")
    emtis("allow")
}
</script>

<style>
.show{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 200px;
    padding: 20px;
    border-radius: 40px;
    font-size: 20px;
    cursor: pointer;
}
</style>