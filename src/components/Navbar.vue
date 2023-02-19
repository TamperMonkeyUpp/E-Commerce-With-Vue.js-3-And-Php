<template>
   <nav class="bg-gray-800 w-full h-16 flex items-center p-3 text-gray-300 justify-between">
        <div class="flex items-center">
            <img src="../assets/logo.svg" class="object-cover w-16 p-1 " alt="">
            <h1 class="text-lg">E - Commerce</h1>
        </div>
        <div class="flex gap-5">
            <router-link :to="{path: '/'}" class="rounded-sm hover:bg-blue-900 p-1 px-2">Home</router-link>
        </div>
        <div class="gap-5 flex">
           <LoginPopup/>
           <RegisterPopup/>
        </div>
    </nav>
</template>

<script>
import RegisterPopup from './popup/navpopup/RegisterPopup.vue';
import LoginPopup from './popup/navpopup/LoginPopup.vue';
export default {
    components:{
        LoginPopup,
        RegisterPopup
    }
}
</script>

<style>

</style>