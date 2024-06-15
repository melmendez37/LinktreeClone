<template>
    <div>
        <p @click="open = true" class="text-center text-zinc-100 font-bold mt-4 text-lg cursor-pointer">Share</p>
        <ShareModal v-model="open"/>
    </div>
</template>

<script setup>
let open = ref(false)
</script>