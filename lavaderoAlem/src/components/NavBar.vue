<script setup>
import { Menu } from '@lucide/vue';

const links = [
  { texto: 'Qué hacemos', href: '#servicios' },
  { texto: 'Mejora tu auto', href: '#mejora' },
  { texto: 'Packs', href: '#packs' },
  { texto: 'Testimonios', href: '#testimonios' },
  { texto: 'Escribinos', href: '#contacto' },
] 

</script>

<template>

    <nav class="flex justify-between p-5 bg-black/70 items-center">

        <div class="flex items-center gap-2">
            <img src="../assets/images/logo.jpeg" alt="Logo" class="rounded-full h-15 ">

            <h1 class="text-white">LavaAutosAlem</h1>
        </div>
    


        <div class="block lg:hidden " id="boton">

            <Menu class="text-white" :size="50"/>

        </div>
        

        <div class="hidden w-full block flex-grow  p-2 rounded-xl lg:flex lg:w-auto lg:ml-20 " id="menu">

            <div class="flex flex-col w-full text-right lg:flex-row lg:justify-evenly" > 

                

            </div>

        </div>
    
    </nav>
        

</template>