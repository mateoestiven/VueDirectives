<script setup>
import { ref } from 'vue'

const users = ["Pepe","Ana","Juana","Lola"]

const isChecked = ref(true)
</script>

<template>

    <ul>
        <li v-for="(user, index) in users" :key="index">{{ index }} {{ user }}</li>
    </ul>
    
    <input type="checkbox" id="check" v-model="isChecked">

    <label for="check">Pinchame</label>

    <div 
        class=" bg-blue-400 text-white rounded py-1 px-2 w-40 mx-auto "
        :class="{'bg-orange-400': isChecked }">
        
        Este es un mensaje
    </div>

    <div v-show="isChecked">
        Este es un mensaje que podria ocultar
    </div>
    <div v-if="false">
        Este es un mensaje que podria ocultar
    </div>
    <div v-else>
        Esto se vio porque no cumplio la condicion del if
    </div>

</template>