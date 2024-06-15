<template>
    <div :class="modelValue ? 'visible' : 'invisible'">
        <div class="bg-black opacity-30 fixed top-0 left-0 w-full h-full z-20"></div>

    <div class="fixed left-0 top-0 z-30 h-full w-full flex items-center">
        <div class="bg-cyan-700 z-40 w-auto m-auto p-4 rounded-sm">
            <div class="flex items-center justify-between mb-10 mt-2">
                <p class="font-bold px-1 text-zinc-100">Share profile</p>
                <button @click="close()" class="flex justify-center items-center rounded-sm hover:bg-zinc-300" type="button">
                    <Icon name="mdi:close" size="20" class="text-zinc-100 hover:text-black"/>
                </button>
            </div>

            <div class="flex items-center justify-between mb-4">
                <div class="flex items-center">
                    <Icon name="mdi:whatsapp" size="20" class="text-zinc-100"/>
                    <a href="https://wa.me?text=helloworld" target="_blank" class="px-2 text-zinc-100">
                        <span class="mr-2 text-lg">Share with whatsapp</span>
                    </a>
                </div>
                <Icon name="mdi:chevron-right" size="30" class="text-zinc-100"/>
            </div>

            <div @click="shareLink()" class="flex justify-between items-center border border-3 border-zinc-100 rounded-lg p-2">
                <Icon name="mdi:content-copy" class="text-zinc-100"/>
                <p class="text-zinc-300 px-2 text-sm">portfolio-22.netlify.com</p>
                <p class="font-bold text-sm text-zinc-100 cursor-pointer hover:text-zinc-300" :class="`${copy === 'Copy' ? 'text-zinc-100' : 'text-green-500'}`">{{copy}}</p>
            </div>
        </div>
    </div>
    </div>
</template>

<script setup>
defineProps(['modelValue']);

const emits =defineEmits(["update:modelValue"]);

let copy = ref("Copy");
function shareLink(){
    navigator.clipboard.writeText("https://sample-site.com")
    copy.value="Copied!"
}

function close() {
    emits("update:modelValue", false)
    copy.value="Copy"
}
</script>