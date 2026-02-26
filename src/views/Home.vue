<template>
    <div class="bg-bg min-h-screen">
        <NavigationBar />

        <!-- HERO -->
        <section class="pt-32 pb-20">
            <div class="max-w-7xl mx-auto px-6 grid md:grid-cols-2 gap-12 items-center">

                <!-- Left Content -->
                <div>
                    <h1 class="text-3xl sm:text-4xl md:text-6xl font-bold leading-tight mb-6">
                        Building <span class="text-accent">scalable</span><br />
                        web & mobile products
                    </h1>

                    <p class="text-gray-400 text-lg mb-8 max-w-xl">
                        Full Stack Developer specializing in Vue, Laravel, and Flutter.
                        I build production-ready dashboards, SaaS platforms, and business systems.
                    </p>

                    <div class="flex flex-wrap gap-3 mb-8">
                        <span class="px-3 py-1 text-sm bg-white/5 rounded-full">Vue.js</span>
                        <span class="px-3 py-1 text-sm bg-white/5 rounded-full">Laravel</span>
                        <span class="px-3 py-1 text-sm bg-white/5 rounded-full">Flutter</span>
                        <span class="px-3 py-1 text-sm bg-white/5 rounded-full">REST APIs</span>
                        <span class="px-3 py-1 text-sm bg-white/5 rounded-full">SaaS</span>
                    </div>

                    <div class="flex flex-col sm:flex-row gap-4">
                        <a href="#projects" class="inline-flex items-center justify-center px-6 py-3 
           bg-accent text-white font-semibold 
           rounded-xl hover:scale-105 hover:brightness-110 transition">
                            View Projects
                        </a>

                        <a href="#contact" class="inline-flex items-center justify-center px-6 py-3 
           border border-accent/40 text-accent 
           rounded-xl hover:bg-accent/10 transition">
                            Contact Me
                        </a>

                        <a href="/resume.pdf" download class="inline-flex items-center justify-center px-6 py-3 
           border border-white/20 text-gray-300 
           rounded-xl hover:bg-white/5 transition">
                            Download Resume
                        </a>
                    </div>
                </div>

                <!-- Right Visual -->
                <div class="hidden md:block">
                    <div class="relative">
                        <div class="absolute -top-10 -left-10 w-72 h-72 bg-accent/20 rounded-full blur-3xl"></div>
                        <div class="relative bg-card p-8 rounded-2xl border border-white/10">
                            <p class="text-sm text-gray-400 mb-2">Currently working with</p>
                            <h3 class="text-xl font-semibold mb-4">Vue · Laravel · Flutter</h3>
                            <p class="text-gray-400 text-sm">
                                5+ years experience building real-world applications used by businesses.
                            </p>
                        </div>
                    </div>
                </div>

            </div>
        </section>
        <!-- PROJECTS -->
        <section id="projects" class="py-24">
            <div class="max-w-7xl mx-auto px-6">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">
                    Selected Projects
                </h2>

                <p class="text-gray-400 mb-12 max-w-2xl">
                    A selection of real-world applications I’ve built for businesses and users.
                </p>

                <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <ProjectCard v-for="project in projects" :key="project.title" :project="project" />
                </div>
            </div>
        </section>
        <div class="h-px bg-white/10 my-24"></div>
        <ExperienceTimeline />
        <div class="h-px bg-white/10 my-24"></div>
        <Services />
        <Contact />
        <Footer />
    </div>
</template>

<script setup>
import ProjectCard from '../components/ProjectCard.vue';
import { projects } from '../data/projects';
import ExperienceTimeline from '../components/ExperienceTimeline.vue';
import Services from '../components/Services.vue';
import Contact from '../components/Contact.vue';
import Footer from '../components/Footer.vue';
import NavigationBar from '../components/NavigationBar.vue';
</script>
