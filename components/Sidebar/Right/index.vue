<template>
    <div class="flex flex-col">
        <!----- Preview Card : What's happening --------->

                <SidebarRightPreviewCard title="What's happening">
                        <SidebarRightPreviewCardItem v-for="whatsHappening in whatsHappeningItems">
                            <h2 class="font-bold text-gray-800 text-md dark:text-white">{{ whatsHappening.title }}</h2>
                            <p class="text-xs text-gray-400">{{ whatsHappening.count }}</p>
                        </SidebarRightPreviewCardItem>
                </SidebarRightPreviewCard>

        <!----- Preview Card : Who to follow  ----------->
                
                <SidebarRightPreviewCard title="Who To follow">
                        <SidebarRightPreviewCardItem v-for="whoToFollow in whotoFollowItems">
                            <div class="flex flex-row items-center justify-between p-2">
                                <div class="flex flex-row">
                                    <img class="w-10 h-10 rounded-full" :src="whoToFollow.image" :alt="whoToFollow.name">

                                    <div class="flex flex-col ml-2">
                                        <h1 class="text-sm font-bold text-gray-900 dark:text-white">{{ whoToFollow.name }}</h1>
                                        <p class="text-xs text-gray-400">{{ whoToFollow.handle }}</p>
                                    </div>
                                </div>
                                <div class="flex h-full">
                                    <button
                                        class="px-4 py-2 text-xs font-bold text-white bg-black rounded-full dark:text-black dark:bg-white">Follow</button>
                                </div>
                            </div>

                        </SidebarRightPreviewCardItem>
                </SidebarRightPreviewCard>

    </div>
</template>

<script setup>
const whatsHappeningItems = ref([
    {
        title: 'SpaceX',
        count: '18.8 Tweets'
    },
    {
        title: '#CodingIsFun',
        count: '18.8 Tweets'
    },
    {
        title: '#ArtforAllm',
        count: '18.8 Tweets'
    }

])
const whotoFollowItems = ref([
    {
        name: 'Jekee',
        handle: '@Jekee',
        image: 'https://picsum.photos/536/354'
    },
    {
        name: 'John David',
        handle: '@johndavid',
        image: 'https://picsum.photos/id/237/536/354'
    },
    {
        name: 'Albert',
        handle: '@Albert',
        image: 'https://picsum.photos/536/354'
    }

])
</script>