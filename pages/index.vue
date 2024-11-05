<template>
    <div class="bg-white min-h-screen">
        HELLO WASSUP!!!
        <UAccordion
            color="primary"
            variant="soft"
            size="sm"
            :items="items"
        />
        <UButton label="Open" @click="isOpen = true" />

        <UModal v-model="isOpen" prevent-close>
            <UCard :ui="{ ring: '', divide: 'divide-y divide-gray-100 dark:divide-gray-800' }">
                <template #header>
                    <div class="flex items-center justify-between">
                        <h3 class="text-base font-semibold leading-6 text-gray-900 dark:text-white">
                        Modal
                        </h3>
                        <UButton color="gray" variant="ghost" icon="i-heroicons-x-mark-20-solid" class="-my-1" @click="isOpen = false" />
                    </div>
                </template>

                <Placeholder class="h-32" />
            </UCard>
        </UModal>
    </div>
</template>

<script setup lang="ts">
    const isOpen = ref(false)
    const items = [{ label: '1. What is Nuxt UI?', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit' }, { label: '2. Getting Started', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit' }, { label: '3. Theming', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit' }, { label: '4. Components', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit' }]
</script>