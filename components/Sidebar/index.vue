<template>
    <div class="h-screen flex flex-col">
        <div class="p-2 my-2 hover:bg-gray-200 dark:hover:bg-white/20 rounded-full w-min" :class="defaultTrasition">
            <nuxt-link to="/">
                <div class="w-8 h-8">
                    <LogoTwitter />
                </div>
            </nuxt-link>
        </div>
        <SidebarLeftTab active>
            <template v-slot:icon>
                <HomeIcon/>
            </template>
            <template v-slot:name>
                Home
            </template>
        </SidebarLeftTab>
        
        <div class="mt-2 space-y-3 "></div>
        
        <SidebarLeftTab>
            <template v-slot:icon>
                <HashtagIcon />
            </template>
            <template v-slot:name>
                Explore
            </template>
        </SidebarLeftTab>

        <div class="mt-2 space-y-3 "></div>
        
        <SidebarLeftTab>
            <template v-slot:icon>
                <BellIcon />
            </template>
            <template v-slot:name>
                Notifications
            </template>
        </SidebarLeftTab>

        <div class="mt-2 space-y-3 "></div>
        
        <SidebarLeftTab>
            <template v-slot:icon>
                <InboxIcon />
            </template>
            <template v-slot:name>
                Messages
            </template>
        </SidebarLeftTab>

        <div class="mt-2 space-y-3 "></div>
        
        <SidebarLeftTab>
            <template v-slot:icon>
                <BookmarkIcon />
            </template>
            <template v-slot:name>
                Bookmarks
            </template>
        </SidebarLeftTab>

        <div class="mt-2 space-y-3 "></div>
        
        <SidebarLeftTab>
            <template v-slot:icon>
                <DocumentTextIcon />
            </template>
            <template v-slot:name>
                lists
            </template>
        </SidebarLeftTab>

        <div class="mt-2 space-y-3 "></div>
        
        <SidebarLeftTab>
            <template v-slot:icon>
                <UserIcon />
            </template>
            <template v-slot:name>
                Profile
            </template>
        </SidebarLeftTab>

        <div class="mt-2 space-y-3 "></div>
        
        <SidebarLeftTab>
            <template v-slot:icon>
                <DotsCircleHorizontalIcon />
            </template>
            <template v-slot:name>
                More
            </template>
        </SidebarLeftTab>

    </div>
</template>

<script setup>

import { HomeIcon } from "@heroicons/vue/solid" 
import { HashtagIcon, BellIcon, InboxIcon, BookmarkIcon, DocumentTextIcon, UserIcon, DotsCircleHorizontalIcon } from "@heroicons/vue/outline" 
const { defaultTrasition } = useTailwindConfig()

</script>