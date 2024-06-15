<template>
    <div class="w-full bg-transparent flex items-center rounded-md border border-zinc-100 p-3 mt-4 max-w-md hover:bg-cyan-800 cursor-pointer" @click="goTo(link.link)">
        <Icon :name="`mdi:${link.icon}`" size="24" class="text-zinc-100"/>
        <p class="font-bold px-1 text-zinc-100">{{ link.text }}</p>
    </div>
</template>

<script setup>
defineProps({
    link:{
        type: Object
    }
});
function goTo(link){
    window.open(link, "_blank");
}
</script>