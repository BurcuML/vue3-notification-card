<script setup>
import Button from "./components/button.vue"
import notification from "./components/notification.vue";
import { ref } from 'vue'

const notifications = ref(false)

const showClick = () => {
  notifications.value = !notifications.value
}

</script>

<template>
 <div class="floor">
  <Button @show="showClick"></Button>
  <notification v-if="notifications"  @close=""></notification>
 </div>
</template>

<style scoped>
.floor{
   position: absolute;
   width: 700px;
   height: 175px;
   top: 50%;
   left: 50%;
   transform: translate(-50%, -50%);
   background-color: rgb(100, 136, 124);
   border-radius: 40px;
}

</style>
