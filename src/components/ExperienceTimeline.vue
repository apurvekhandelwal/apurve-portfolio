<template>
    <section id="experience" class="py-24">
        <div class="max-w-7xl mx-auto px-6">
            <h2 class="text-3xl md:text-4xl font-bold mb-12">
                Experience
            </h2>

            <div class="relative pl-6 sm:pl-8 space-y-10 sm:space-y-12">
                <div
                    class="absolute left-0 top-0 h-full w-px bg-gradient-to-b from-accent/40 via-white/10 to-transparent">
                </div>
                <div v-for="item in experience" :key="item.company" class="relative">
                    <!-- Dot -->
                    <span
                        class="absolute -left-[11px] top-2 w-5 h-5 rounded-full bg-accent ring-4 ring-accent/20"></span>


                    <!-- Content -->
                    <div
                        class="bg-card border border-white/10 rounded-2xl p-6 transition hover:border-accent/30 hover:shadow-lg">

                        <div class="flex flex-col md:flex-row md:items-center md:justify-between mb-2">
                            <h3 class="text-lg font-semibold">
                                {{ item.role }}
                            </h3>
                            <span class="text-sm text-gray-400">
                                {{ item.duration }}
                            </span>
                        </div>

                        <p class="text-accent text-sm mb-3">
                            {{ item.company }}
                        </p>

                        <p class="text-gray-400 text-sm leading-relaxed">
                            {{ item.description }}
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { experience } from '../data/experience'
</script>
