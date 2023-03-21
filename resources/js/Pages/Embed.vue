<script setup>
import { Head } from "@inertiajs/vue3";
import { TabGroup, TabList, Tab, TabPanels, TabPanel } from '@headlessui/vue'
import ApplicationCard from "@/Components/ApplicationCard.vue";

const props = defineProps({
    apps: Object
});

</script>
<template>
    <Head>
        <title>Embed</title>
    </Head>
    <div class="grid grid-cols-3 p-5 gap-4">
        <application-card class="h-72" v-for="app in apps" :app="app" />
    </div>
<!--    <div class="w-full sm:px-0">-->
<!--        <TabGroup>-->
<!--            <TabList class="flex space-x-1 bg-black/80">-->
<!--                <Tab-->
<!--                    v-for="category in Object.keys(apps)"-->
<!--                    as="template"-->
<!--                    :key="category"-->
<!--                    v-slot="{ selected }"-->
<!--                >-->
<!--                    <button-->
<!--                        :class="[-->
<!--              'w-full py-2 text-sm font-medium leading-5 text-white focus:ring-transparent',-->
<!--              selected-->
<!--                ? 'bg-black/90'-->
<!--                : '',-->
<!--            ]"-->
<!--                    >-->
<!--                        {{ category }}-->
<!--                    </button>-->
<!--                </Tab>-->
<!--            </TabList>-->

<!--            <TabPanels>-->
<!--                <TabPanel-->
<!--                    v-for="(posts, idx) in Object.values(apps)"-->
<!--                    :key="idx"-->
<!--                    class="h-screen"-->
<!--                >-->
<!--                    <iframe v-for="post in posts" height="100%" width="100%" allowfullscreen :src="post.link" />-->
<!--                </TabPanel>-->
<!--            </TabPanels>-->
<!--        </TabGroup>-->
<!--    </div>-->
</template>
