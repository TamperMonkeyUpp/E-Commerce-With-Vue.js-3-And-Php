<template>
 <button @click="showPopup = true" class="rounded-sm hover:bg-blue-900 p-1 px-2">Register</button>
 <transition class="popup">
    <div v-if="showPopup">
      <div  class="w-96 mx-auto mt-14">
        <h1 class="text-center text-3xl mb-5">Register</h1>
        <form @submit.prevent="" class="flex-col flex gap-5 p-2 text-gray-900">
            <input type="text" class="form-input rounded-sm outline-none h-10 p-2" placeholder="Enter Username">
            <input type="username" class="form-input rounded-sm outline-none h-10 p-2" placeholder="Enter Name And Lastname">
            <input type="email" class="form-input rounded-sm outline-none h-10 p-2" placeholder="Enter E-Mail">
            <input type="password" class="form-input rounded-sm outline-none h-10 p-2" placeholder="Enter Password">
            <input type="password" class="form-input rounded-sm outline-none h-10 p-2" placeholder="Enter Re-Password">
            <div class="text-gray-300 flex justify-center items-center gap-2 mt-1 py-5">
                <button class="w-2/4 bg-teal-800   rounded-sm p-1">Register</button>
                <button @click="closePopup" class="bg-red-700 text-white w-2/4 text-center p-1 rounded-sm">X</button>
            </div>
            
        </form>
      </div>
    </div>
  </transition>

</template>

<script>
import {ref} from 'vue';
export default {
  setup(){
    //popup ------
    let showPopup = ref(false);
    function closePopup(){
      showPopup.value = false;
    }
    //------------

    

    return {showPopup, closePopup}
  }
}
</script>

<style scoped>
.popup{
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 1;
  background: #111111bb;
  padding: 0px 20px;
}
</style>