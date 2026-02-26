<template>
    <header class="fixed top-0 w-full z-50 bg-bg/80 backdrop-blur border-b border-white/10">
        <nav class="max-w-7xl mx-auto px-6 py-4 flex items-center justify-between">
            <!-- Logo / Name -->
            <div class="text-lg font-semibold tracking-wide">
                Apurve<span class="text-accent">.</span>
            </div>

            <!-- Navigation -->
            <ul class="hidden md:flex items-center gap-8 text-sm text-gray-300">
                <li><a href="#projects" class="hover:text-white transition">Projects</a></li>
                <li><a href="#experience" class="hover:text-white transition">Experience</a></li>
                <li><a href="#contact" class="hover:text-white transition">Contact</a></li>
            </ul>

            <!-- CTA -->
            <a href="#contact" class="hidden md:inline-flex items-center justify-center 
         px-5 py-2 rounded-xl 
         bg-accent text-white font-medium 
         hover:scale-105 hover:brightness-110 transition">
                Hire Me
            </a>
            <div v-if="open" class="md:hidden bg-bg border-t border-white/10">
                <div class="px-6 py-4 space-y-4">
                    <a href="#projects" @click="open = false" class="block">Projects</a>
                    <a href="#experience" @click="open = false" class="block">Experience</a>
                    <a href="#contact" @click="open = false" class="block">Contact</a>
                </div>
            </div>

            <button class="md:hidden text-gray-300" @click="open = !open">
                ☰
            </button>
        </nav>
    </header>
</template>

<script setup>
import { ref } from 'vue'
const open = ref(false)
</script>
