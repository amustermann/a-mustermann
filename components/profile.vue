<template>
    <div class="w-full md:w-[48rem] rounded-md overflow-clip">
        <main class="card w-full md:w-[48rem] p-5">
            <div class="flex mb-4 items-center">
                <img class="w-20 h-20 md:h-28 md:w-28 rounded-md mr-4"
                src="https://cdn.discordapp.com/avatars/766649339538964520/ae8dad1aa3466b3929debca00ce1103c.webp?size=240" />
                <div class="flex flex-col justify-center">
                    <h1 class="text-4xl font-bold">a.mustermann</h1>
                    <h2 class="text-xl text-gray-300">Pro Counter-Strike player</h2>
                </div>
            </div>
            <!-- quote -->
            <div class="bg-[#8e502991] rounded-md p-2 px-4 relative">
                <NuxtIcon name="quote" class="absolute -top-2 -right-2 scale-[180%] [&>path]:stroke-none" filled></NuxtIcon>
                <p class="text-lg">
                    Schon im jungen Alter von 10 Jahren begann der legendäre Mustermann seine CS-Karriere, heutzutage ist er als
                    Legende unter allen Vertigo-Spielern bekannt.
                    Seine unglaublichen no-scopes setzen bis heute einen neuen Standard für “Ohne-Rohr Schüsse”.
                </p>
            </div>
        </main>
    </div>
</template>
