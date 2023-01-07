<template>
    <div>
        <nuxt-link to="#" class="flex items-center p-3 w-min text-black hover:bg-gray-200 dark:hover:bg-dim-200 dark:text-white rounded-full">
            
            <div class="w-6 h-6 text-dark" :class="defaultTrasition">
                <slot name="icon"></slot>
            </div>
            <div class="ml-4 text-xl xl:block hidden" :class="textClass">
                <slot name="name"></slot>
            </div>
            
        </nuxt-link>
    </div>
</template>

<script setup>
const { defaultTrasition } = useTailwindConfig()

const props = defineProps({
    active: {
        type: Boolean,
        default: false
    }

})

const textClass = computed(() => props.active ? 'font-semibold' : 'font-normal')

</script>