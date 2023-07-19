<script setup>
import { toRefs, ref } from "vue";
import { RouterLink } from "vue-router";
import Play from 'vue-material-design-icons/play.vue'

let isHover = ref(false)

const props = defineProps({
    category: String,
    images: Object,
    text: String,
    to: String
})
const { category, images, text, to } = toRefs(props)



</script>
<template>
    <div class="">
        <RouterLink
            :to="to"
            class="relative"
        >
            <div 
                @mouseenter="$event => isHover = true"
                @mouseleave="$event => isHover = false"
                class="flex justify-center contrast-[2] brightness-[0.87] rounded-md aspect-square overflow-hidden"
            >
                <div 
                :class="isHover ? 'transition ease-in duration-150 bg-opacity-20' : 'transition ease-out duration-150 bg-opacity-5'"
                    class="absolute w-full h-full bg-black z-10 rounded-md"
                />
                <img 
                    class="absolute contrast-[0.55] right-0 top-0 w-1/2"
                    :src="images.one" alt=""
                >
                <img 
                    class="absolute contrast-[0.55] left-0 top-0 w-1/2"
                    :src="images.two" alt=""
                >
                <img 
                    class="absolute contrast-[0.55] right-0 bottom-0 w-1/2"
                    :src="images.three" alt=""
                >
                <img 
                    class="absolute contrast-[0.55] left-0 bottom-0 w-1/2"
                    :src="images.four" alt=""
                >
                <div class="absolute top-[43%] z-10 p-2 rounded-full bg-white inline-block">
                    <Play :size="33" />
                </div>
                <div class="absolute z-10 flex items-center bottom-1 left-0 h-7 bg-bloack rounded-full px-2 bg-opacity-10">
                    <img 
                        class=" pr-2 opacity-[0.75] brightness-[1.2]"
                        src="/images/deezer-sound-icon.png"
                        width="30"
                    >
                    <div class="text-white font-bold text-[21px]">{{ category }}</div>
                </div>

            </div>   
        </RouterLink>
        <div class="h-2"></div>
        <RouterLink :to="to">
            <div class="hover:underline capitalize text-gray-200 font-light text-sm">
                {{ text }}
            </div>
        </RouterLink>
    </div>
</template>

