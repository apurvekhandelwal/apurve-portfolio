<template>
    <div
        class="bg-card border border-white/10 rounded-2xl p-6 h-full flex flex-col hover:-translate-y-2 hover:shadow-xl transition-all duration-300">
        <h3 class="text-xl font-semibold mb-3">
            {{ project.title }}
        </h3>

        <p class="text-gray-400 text-sm mb-4">
            {{ project.description }}
        </p>

        <div class="flex flex-wrap gap-2 mb-6">
            <span v-for="tech in project.tech" :key="tech"
                class="text-xs px-3 py-1 rounded-full bg-white/10 text-gray-300">
                {{ tech }}
            </span>
        </div>

        <a :href="project.link" target="_blank"
            class="mt-auto inline-block text-accent text-sm font-medium hover:underline">
            View Project →
        </a>
    </div>
</template>

<script setup>
defineProps({
    project: {
        type: Object,
        required: true,
    },
})
</script>
