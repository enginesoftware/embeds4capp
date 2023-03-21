<script setup>
defineProps({
    app: Object
})
</script>
<template>
    <div class="overflow-hidden rounded-lg shadow transition hover:shadow-lg">
<!--        <img-->
<!--            alt="Office"-->
<!--            src="https://images.unsplash.com/photo-1524758631624-e2822e304c36?ixlib=rb-1.2.1&ixid=MnwxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2070&q=80"-->
<!--            class="h-56 w-full object-cover"-->
<!--        />-->
        <div class="flex justify-center">
            <img class="h-48 w-48 rounded-full" :src="['https://ui-avatars.com/api/?name=' + app.name +'&background=random&bold=true&size=128']" alt=""/>
        </div>

        <div class="bg-white p-4 sm:p-6">
<!--            <time datetime="2022-10-10" class="block text-xs text-gray-500">-->
<!--                10th Oct 2022-->
<!--            </time>-->

            <a :href="app.link" target="_blank">
                <h3 class="mt-0.5 text-center text-2xl text-gray-900">
                    {{ app.name || 'Sistema Sem Nome' }}
                </h3>
            </a>

<!--            <p class="mt-2 text-sm leading-relaxed text-gray-500 line-clamp-3">-->
<!--                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Recusandae-->
<!--                dolores, possimus pariatur animi temporibus nesciunt praesentium dolore-->
<!--                sed nulla ipsum eveniet corporis quidem, mollitia itaque minus soluta,-->
<!--                voluptates neque explicabo tempora nisi culpa eius atque dignissimos.-->
<!--                Molestias explicabo corporis voluptatem?-->
<!--            </p>-->
        </div>
    </div>
</template>
