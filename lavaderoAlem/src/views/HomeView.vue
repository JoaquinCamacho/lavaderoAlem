<script setup>
import { ref, onMounted } from 'vue'

const wsp = "https://wa.me/5491154139603?text=Hola!%20Quiero%20reservar%20un%20turno"

const videoHero = ref(null)

onMounted(() => {
    videoHero.value.playbackRate = 2
})

</script>

<template>
    
    <section class="min-h-screen bg-linear-to-b from-neutral-950 to-green-950 text-white pt-35">

        <div class="flex justify-center gap-4  px-3 py-2 bg-white/10 backdrop-opacity-10 w-fit mx-auto rounded-2xl border-green-200 border-2 titulo text-center items-center lg:text-2xl">

        <span class="relative flex h-3 w-3">
            <span class="absolute inline-flex h-full w-full animate-ping rounded-full bg-green-400 opacity-75"></span>
            <span class="relative inline-flex h-3 w-3 rounded-full bg-green-500"></span>
        </span>

            <h1>
                Agenda abierta - Burzaco
            </h1>


        </div>

        <div class="flex flex-col justify-center text-center pt-5 gap-5 mx-auto max-w-3xl px-4">
            <h2 class="titulo text-4xl font-extrabold lg:text-7xl">Detailing y lavado profesional en Burzaco.</h2>
            <p class="texto mx-auto max-w-xl text-lg text-white/60 lg:text-2xl">Lavado artesanal al detalle, tu pintura limpia, brillante y sin marcas. </p>
            
            <div class="flex flex-col gap-4 justify-center items-center lg:flex-row lg:justify-">
                <a :href="wsp" target="_blank" class="titulo p-3 rounded-lg text-black bg-green-500 w-fit  mt-4 lg:mt-0 lg:self-auto transition duration-300 lg:hover:bg-green-400 lg:hover:scale-105 lg:hover:shadow-lg lg:hover:shadow-green-500/50 lg:text-lg">Reserva por WhatsApp</a>
                <a href="" class="p-3 bg-white/10 backdrop-opacity-10 w-fit rounded-2xl border-green-200 border-2 titulo lg:mt-0 lg:self-auto transition duration-300 lg:hover:bg-white-400 lg:hover:scale-105 lg:hover:shadow-lg ">Ver Packs</a>
            </div>
        </div>

        <div class="mx-4 py-2 h-100 lg:mx-auto lg:max-w-4xl rounded-lg bg-white/10 px-5">
            
            <video src="../assets/images/videoHero.mp4" autoplay muted loop playsinline  class="w-full h-full rounded-lg "></video>
        </div>
        
    </section>


</template>