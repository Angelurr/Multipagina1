<script setup>
import { ref } from 'vue';
let qty =ref(0);
function add (){
    qty.value++
    console.log(qty)
}
function resta(){
    qty.value--
    console.log(qty)
}
</script>
<template>
    <div class="bg-purple-300 max-w-80 p-6 mx-auto rounded">
        <div 
        v-if="qty > 0"
        class="bg-red-500 text-white size-6 rounded-full flex justify-center items-center font-bold" :class="{'bg-orange-500': qty > 3}">
        
            {{ qty }}

        </div>
        <div v-else >
            Nadie te visita :(

        </div>        
        <div 
        @click="add"
        class="bg-blue-400 text-white rounded size-6 flex justify-center items-center">
           
            +

        </div>
        <div 
        
        @click="resta"
        class="bg-blue-400 text-white rounded size-6 flex justify-center items-center">
           
            -

        </div>

    </div>
</template>