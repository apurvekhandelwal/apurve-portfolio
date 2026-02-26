<template>
    <footer class="border-t border-white/10 py-10">
        <div class="max-w-7xl mx-auto px-6 flex flex-col md:flex-row gap-6 items-center justify-between">

            <!-- Left -->
            <p class="text-sm text-gray-400">
                © {{ year }} Apurve Khandelwal. All rights reserved.
            </p>

            <!-- Right -->
            <div class="flex gap-6 text-sm">
                <a href="https://github.com/" target="_blank" class="text-gray-400 hover:text-white transition">
                    GitHub
                </a>

                <a href="https://www.linkedin.com/in/apurve-khandelwal-759b761b2/" target="_blank"
                    class="text-gray-400 hover:text-white transition">
                    LinkedIn
                </a>
            </div>

        </div>
    </footer>
</template>

<script setup>
const year = new Date().getFullYear()
</script>
