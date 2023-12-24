<template>
    <div class="w-full md:w-[48rem] rounded-md overflow-clip">
        <main class="card w-full md:w-[48rem] p-5 px-6 !bg-[#8e5029cc]">
            <div class="flex justify-between">
                <span>
                    <h1 class="text-xl font-bold inline-flex items-center mb-6 h-6">Links</h1>
                    <NuxtIcon name="link" class="ml-2 inline-block h-4" />
                </span>
                <button class="h-full w-8" @click="rickRoll()">
                    <NuxtIcon name="smile" filled class="h-6 text-3xl" />
                </button>
            </div>
            <ul class="flex justify-between">
                <li v-for="link in links"
                    class="bg-[#FFE1C5] h-28 w-28 rounded-md mx-1 first:mx-0 first:mr-1 last:mx-0 last:ml-1">
                    <a :href="link.url" target="_blank" class="w-full h-full flex justify-center items-center">
                        <NuxtIcon :name="link.icon" filled class="text-4xl sm:text-7xl" />
                    </a>
                </li>
            </ul>
        </main>
    </div>
</template>

<style scoped>
li {
    transition: all 0.3s ease-in-out;
}

li:hover {
    background: #FFD8B0;
    transform: scale3d(1.05, 1.05, 1.05);
    box-shadow: rgba(50, 50, 93, 0.25) 0px 50px 100px -20px, rgba(0, 0, 0, 0.463) 0px 30px 60px -30px;
}

li:active {
    transform: scale3d(0.95, 0.95, 0.95);
    box-shadow: rgba(50, 50, 93, 0.25) 0px 50px 100px -20px, rgba(0, 0, 0, 0.3) 0px 30px 60px -30px;
}
</style>

<script lang="ts" setup>
const links:
    {
        name: string
        url: string
        icon: string
    }[]
    = [
        {
            name: 'Steam',
            url: 'https://steamcommunity.com/id/amustermann',
            icon: 'steam'
        },
        {
            name: 'YouTube',
            url: 'https://www.youtube.com/channel/UCUcV1kkAI-FBq87aa0qIFlA',
            icon: 'youtube'
        },
        {
            name: 'TradeURL',
            url: 'https://steamcommunity.com/tradeoffer/new/?partner=108660871',
            icon: 'trade'
        },
        {
            name: 'SteamLadder',
            url: 'https://steamladder.com/profile/76561198068926599',
            icon: 'ladder'
        },
        {
            name: 'SteamRep',
            url: 'https://steamrep.com/profiles/76561198068926599',
            icon: 'rep'
        }
    ]

const rickRoll = () => {
    window.open('https://www.youtube.com/watch?v=dQw4w9WgXcQ', '_blank')
}
</script>