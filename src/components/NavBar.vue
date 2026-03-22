<script setup lang="ts">
import { ref } from 'vue';
// icons
import { ChevronDownIcon } from '@heroicons/vue/16/solid';
import { Bars2Icon, XMarkIcon } from '@heroicons/vue/24/outline';
// component
import { Dialog, DialogPanel } from '@headlessui/vue';

// Menu mobile open
const mobileOpenMenu = ref(false)
</script>

<template>
    <nav class="fixed top-0 left-0 w-full z-20">
        <div class="max-w-7xl mx-auto px-6 md:px-12">
            <div class="flex items-center justify-between lg:h-30 h-19">
                <a href="" class="flex items-center space-x-2.5">
                    <img src=".././assets/Bento.svg" class="h-7" alt="Bento" />
                    <span class="text-xl font-bold ">Bento.</span>
                </a>

                <div class="flex lg:hidden">
                    <button type="button"
                        class="-mt-2.5 inline-flex items-center p-2.5 justify-center  rounded-xl  bg-white/45"
                        @click="mobileOpenMenu = true">
                        <span class="sr-only">Open main menu</span>
                        <Bars2Icon class="size-6" aria-hidden="true" />
                    </button>
                </div>


                <div class="hidden lg:flex lg:gap-x-12">
                    <a class="block py-2 px-2 text-black md:p-0" aria-current="page">Home</a>
                    <a href="" class="block py-2 px-3 text-black/65 hover:text-black md:p-0 hover:bg-white/5">
                        <span class="flex items-center space-x-1.5">
                            Discover
                            <ChevronDownIcon class="size-6" />
                        </span>

                    </a>
                    <a href="" class="block py-2  text-black/65 hover:text-black md:p-0 hover:bg-white/5">Service</a>
                    <a href="" class="block py-2  text-black/65 hover:text-black md:p-0 hover:bg-white/5">About</a>
                </div>

                <div class=" hidden lg:flex lg:justify-end">
                    <button type="button"
                        class="bg-[#252525] text-white/75 font-semibold drop-shadow-xl drop-shadow-slate-950/30 cursor-pointer hover:bg-zinc-900  rounded-xl py-2.5 px-6">
                        Sign In
                    </button>
                </div>

            </div>
        </div>

    </nav>

    <Dialog class="lg:hidden" @close="mobileOpenMenu = false" :open="mobileOpenMenu">
        <div class="fixed inset-0 z-50"></div>
        <DialogPanel class="fixed inset-y-0 right-0 z-50 w-full overflow-auto  p-6 
                        " style="background: linear-gradient(110.55deg, #FBF2DD 1.4%, #FFD77E 98.6%);">
            <div class="flex items-center justify-between h-18">
                <a href="" class="flex items-center space-x-2.5">
                    <img src=".././assets/Bento.svg" class="h-7" alt="Bento" />
                    <span class="text-xl font-bold ">Bento.</span>
                </a>
                <button type="button" @click="mobileOpenMenu = false" class=" -m-2.5 p-2 rounded-xl bg-neutral-100/40">
                    <span class="sr-only">Close menu</span>
                    <XMarkIcon class="size-6" />
                </button>
            </div>
            <div class="mt-6 flow-root">
                <div class="-my-6 divide-y"></div>
                <div class="space-y-2 py-6">
                    <a class="block py-2 px-2 text-black md:p-0" aria-current="page">Home</a>
                    <a href="" class="block py-2 px-3 text-black/65 hover:text-black md:p-0">
                        <span class="flex items-center space-x-1.5">
                            Discover
                            <ChevronDownIcon class="size-6" />
                        </span>
                    </a>
                    <a href="" class="block py-2  text-black/65 hover:text-black md:p-0">Service</a>
                    <a href="" class="block py-2  text-black/65 hover:text-black md:p-0">About</a>
                </div>
                <div class="py-6">
                    <button type="button"
                        class="bg-[#252525] text-white/75 font-semibold drop-shadow-xl drop-shadow-slate-950/30 cursor-pointer hover:bg-zinc-900  rounded-xl py-2.5 px-6">
                        Sign In
                    </button>
                </div>
            </div>
        </DialogPanel>
    </Dialog>
</template>