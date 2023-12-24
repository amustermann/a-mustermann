<template>
  <div id="blobs" class="absolute h-screen w-screen inline-block select-none overflow-clip p-0">
    <Blob class="absolute -top-1/4 -left-1/2 md:top-12 md:left-36" />
    <Blob class="absolute -bottom-1/4 md:-bottom-52 -right-3/4 md:right-28" />
  </div>
  <main
    class="w-screen h-screen inline-flex flex-col justify-center overflow-y-scroll items-center relative p-0 px-2 md:px-0">
    <Profile class="mb-12 mt-64 sm:mt-0 sm:mb-20" />
    <Links />
  </main>
</template>

<style>
* {
  color: white;
}

html {
  background: #3A1502;
}

.blob {
  animation: blob 10s infinite;
}

@keyframes blob {
  0% {
    transform: translate(0px, 0px) scale(1);
  }

  33% {
    transform: translate(30px, -50px) scale(1.1);
  }

  66% {
    transform: translate(-20px, 20px) scale(0.9);
  }

  100% {
    transform: translate(0px, 0px) scale(1);
  }
}

.card {
  border-width: .5rem;
  border-style: solid;
  border-image-slice: 1;
  border-image-source: radial-gradient(circle, rgba(220, 150, 86, 1) 0%, rgba(186, 91, 33, 1) 83%);
  background: rgba(99, 45, 12, 0.71);
  backdrop-filter: blur(6px);
  border-radius: 0.625rem;
}

.nuxt-icon svg {
  margin-bottom: 0 !important;
}
</style>