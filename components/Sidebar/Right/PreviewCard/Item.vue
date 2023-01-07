<template>
    <div class="p-3 border-b cursor-pointer hover:bg-gray-100 dark:text-white dark:hover:bg-dim-300" :class="wrapperClasses">
        <slot></slot>
    </div>
</template>

<script setup> 
const { defaultTransition, twitterBorderColor } = useTailwindConfig()

// if we add both classes in one div 
const wrapperClasses = computed(() => `${defaultTransition} ${twitterBorderColor}`)
</script>