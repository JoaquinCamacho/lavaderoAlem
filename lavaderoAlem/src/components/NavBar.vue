<script setup>
import { Menu, X } from '@lucide/vue';
import { ref } from 'vue';


const abierto = ref(false)

const links = [
  { texto: '¿Qué hacemos?', href: '#servicios' },
  { texto: 'Mejora tu auto', href: '#mejora' },
  { texto: 'Packs', href: '#packs' },
  { texto: 'Testimonios', href: '#testimonios' },
] 

</script>

<template>
    <nav class="flex flex-wrap justify-between px-4 py-4 bg-black/75 items-center shadow-md shadow-green-200">


        <img src="../assets/images/logo.jpeg" alt="Logo" class="rounded-full h-16 w-16 lg:h-20 lg:w-20" />

    <button class="lg:hidden" aria-label="Abrir menú" @click="abierto = !abierto">

        <X v-if="abierto" class="text-white" :size="40" />


        <Menu v-else class="text-white" :size="40" />

    </button>

        <div :class="abierto ? 'flex' : 'hidden'" class="w-full grow flex-col p-2 rounded-xl lg:flex lg:flex-row lg:w-auto lg:ml-20">

            <div class="flex flex-col gap-3 w-full text-right text-white lg:flex-row lg:justify-center lg:grow">
            
                <a v-for="link in links" :key="link.href" :href="link.href" @click="abierto = false" class="titulo border-b-1 border-green-200 mt-3 lg:hover:text-green-600 lg:border-none px-2 transition duration-300 lg:relative lg:after:absolute lg:after:left-0 lg:after:-bottom-0 lg:after:h-0.5 lg:after:w-0 lg:after:bg-green-500 lg:after:transition-all lg:after:duration-300 lg:hover:after:w-full">
  {{ link.texto }}
</a>
        
            </div>

            
            <a href="" class="titulo p-3 rounded-lg text-black bg-green-500 w-fit self-end mt-4 lg:mt-0 lg:self-auto transition duration-300 lg:hover:bg-green-400 lg:hover:scale-105 lg:hover:shadow-lg lg:hover:shadow-green-500/50">Escribinos!</a>
        </div>

    </nav>
</template>