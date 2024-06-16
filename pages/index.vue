<template>
    <div class="w-full h-screen bg-cyan-700">

        <div class="flex justify-center items-center">
            <Avatar/>
        </div>

        <div class="text-zinc-100 text-center text-lg mt-4">
            <h1 class="font-bold">@mel.mendez37</h1>
            <h2>Welcome to the landing page!</h2>
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
            link: 'https://www.linkedin.com/in/mendezmelangelo/',
            text: 'LinkedIn',
            icon: 'linkedin'
        },
        {
            link: 'https://github.com/melmendez37',
            text: 'Github',
            icon: 'github'
        },
        {
            link: 'https://www.instagram.com/anjiromeru/',
            text: 'Instagram',
            icon: 'instagram'
        },
        {
            link: 'https://www.youtube.com/@melmendezmusic',
            text: 'YouTube',
            icon: 'youtube'
        },
        {
            link: 'https://www.facebook.com/melangelo.mendez15',
            text: 'Facebook',
            icon: 'facebook'
        },
        
    ]
</script>