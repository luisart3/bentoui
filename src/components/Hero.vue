<script setup lang="ts">


</script>

<template>
    <section class="h-full pt-24  md:pt-14 flex items-center">
        <div class="grid grid-cols-1 md:grid-cols-2 gap:6 md:gap-12 items-center ">
            <div class="flex flex-col space-y-6">
                <h2
                    class="font-['Rubik']! font-semibold  text-[#2E2E2E] text-3xl sm:text-4xl md:text-5xl lg:text-6xl text-balance tracking-tight leading-tight">
                    Your Dream, Our Design.</h2>
                <p class="text-base  sm:text-lg md:text-xl text-black/65 leading-relaxed text-balance ">Elegant,
                    modern, and personalized interior designs that bring comfort and style together.</p>
                <div class="relative max-w-sm">
                    <input id="email" type="email" autocomplete="email" name="email"
                        class="block bg-white py-3 md:py-4 pl-5 pr-28 w-full rounded-2xl outline-1 -outline-offset-1 outline-white/20 focus:-outline-offset-2 focus:outline-white "
                        placeholder="Enter your emial" />
                    <button type="button"
                        class="absolute top-1/2 right-2 cursor-pointer -translate-y-1/2 bg-[#E3ED2F] hover:bg-[#e3f252] text-lime-950 font-medium md:h-12 w-30 h-10  rounded-xl">
                        Get Started</button>
                </div>
            </div>
            <div class="md:max-h-[80vh]  min-h-[40vh] w-full ">
                <img src="/img1.png" class="h-full w-full object-cover " alt="3D image" />
            </div>
        </div>
        
    </section>
</template>