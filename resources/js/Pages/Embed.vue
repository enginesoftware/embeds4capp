<script setup>
import { Head } from "@inertiajs/vue3";
import { TabGroup, TabList, Tab, TabPanels, TabPanel } from '@headlessui/vue'

const props = defineProps({
    apps: Object
});

</script>
<template>
    <Head>
        <title>Embed</title>
    </Head>
    <div class="w-full sm:px-0">
        <TabGroup>
            <TabList class="flex space-x-1 bg-gray-900">
                <Tab
                    v-for="category in Object.keys(apps)"
                    as="template"
                    :key="category"
                    v-slot="{ selected }"
                >
                    <button
                        :class="[
              'w-full py-2.5 text-sm font-medium leading-5 text-white',
              selected
                ? 'bg-white shadow text-gray-900'
                : 'text-white hover:bg-white/[0.12] hover:text-white',
            ]"
                    >
                        {{ category }}
                    </button>
                </Tab>
            </TabList>

            <TabPanels>
                <TabPanel
                    v-for="(posts, idx) in Object.values(apps)"
                    :key="idx"
                    static
                    class="h-screen"
                >
                    <iframe v-for="post in posts" height="100%" width="100%" allowfullscreen :src="post.link" />
                </TabPanel>
            </TabPanels>
        </TabGroup>
    </div>
</template>
