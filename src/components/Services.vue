<template>
    <section id="services" class="py-24">
        <div class="max-w-7xl mx-auto px-6">
            <h2 class="text-3xl md:text-4xl font-bold mb-4">
                Services
            </h2>

            <p class="text-gray-400 mb-12 max-w-2xl">
                I help companies and startups build scalable, production-ready web and mobile applications.
            </p>

            <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6 sm:gap-8">
                <div v-for="service in services" :key="service.title"
                    class="bg-card border border-white/10 rounded-2xl p-6 hover:border-accent/30 hover:shadow-lg transition">
                    <h3 class="text-lg font-semibold mb-3">
                        {{ service.title }}
                    </h3>

                    <p class="text-gray-400 text-sm leading-relaxed">
                        {{ service.description }}
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
const services = [
    {
        title: "Admin Dashboards & SaaS Platforms",
        description:
            "Design and development of scalable admin panels and SaaS platforms using Vue.js and Laravel with clean UX and role-based access.",
    },
    {
        title: "Warehouse & Inventory Systems",
        description:
            "Custom warehouse, inventory, and order management systems built for real business workflows.",
    },
    {
        title: "Flutter Mobile Applications",
        description:
            "Cross-platform mobile apps with Flutter, including API integration, real-time features, and payments.",
    },
    {
        title: "API Development & Integration",
        description:
            "Secure and scalable REST APIs with Laravel, including authentication, integrations, and performance optimization.",
    },
    {
        title: "Frontend Architecture & UX",
        description:
            "Modern frontend architecture with Vue.js, focusing on performance, maintainability, and user experience.",
    },
    {
        title: "Maintenance & Feature Enhancements",
        description:
            "Ongoing support, performance improvements, and feature additions for existing applications.",
    },
]
</script>
