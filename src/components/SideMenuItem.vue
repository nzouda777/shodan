<script setup>
import { toRefs, ref, watchEffect } from "vue";
import { RouterLink, useRouter } from "vue-router";

const route = useRouter()

const props = defineProps({
    iconString: String,
    iconSize: Number,
    pageUrl: String,
    name: String
})

const { iconString, pageUrl, name} = toRefs(props)
let icon = ref(null)

watchEffect( () => {
    if (route.currentRoute.value.path == pageUrl.value && icon.value === iconString.value + '-red') return

    if(route.currentRoute.value.path == pageUrl.value){
        icon.value = iconString.value + '-red'
    }else {
        icon.value = iconString.value + '-white'
    }
    const isHover = () => {
        if(icon.value == iconString.value + '-red'){
            icon.value = iconString.value + '-white'
        }else if(icon.value == iconString.value + '-white'){
            icon.value = iconString.value + '-red'
        }
    }
})
console.log(pageUrl)
console.log()
</script>
<template>
    <div class="flex items-center w-full my-[20px]">
        <RouterLink
            :to="pageUrl"
            :class="pageUrl === route.currentRoute.value.path ? 'border-l-[#EF5465] text-[#EF5465]' : 'border-l-[#191922] text-[#FFFFFF]'"
            class="border-l-4 w-full hover:text-[#EF5465]"
            @mouseenter="$event => isHover()"
            @mouseleave="$event => isHover()"
        >
            <div class="flex items-center pl-3 mx-3 cursor-pointer">
                <img :src="`/images/icons/${icon}.png`" :width="iconSize" alt="">
                <div class="pl-3.5 font-[600] text-[17px]">
                    {{ name }}
                </div>
            </div>
        </RouterLink>
    </div>
</template>

