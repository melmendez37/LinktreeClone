<template>
    <div class="w-full h-screen bg-cyan-700">

        <div class="flex justify-center items-center">
            <Avatar/>
        </div>

        <div class="text-zinc-100 text-center text-lg mt-4">
            <h1 class="font-bold">@mel.mendez37</h1>
            <h2>The Landing Page</h2>
        </div>
        <div class="flex flex-col items-center">
            <CardLinks v-for="(link, idx) in links" :key="idx" :link="link" class="flex justify-center mt-4"/>
        </div>

        <Share />
    </div>
</template>

<script setup>
    const links = [
        {
            link: 'https://www.linkedin.com/',
            text: 'LinkedIn',
            icon: 'linkedin'
        },
        {
            link: 'https://www.github.com/',
            text: 'Github',
            icon: 'github'
        },
        {
            link: 'https://www.youtube.com/',
            text: 'YouTube',
            icon: 'youtube'
        },
        {
            link: 'https://www.facebook.com/',
            text: 'Facebook',
            icon: 'facebook'
        },
        
    ]
</script>