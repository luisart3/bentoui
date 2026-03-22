<script setup lang="ts">
import NavBar from './components/NavBar.vue';
import Hero from './components/Hero.vue';

</script>

<template>
  <div id="app" class="h-full">
    <div class=" max-w-7xl mx-auto px-6 md:px-12 h-full">
      <NavBar />
      <!-- Shapes main-->
      <div class="fixed inset-0 -z-10 pointer-events-none">
        <div class="absolute top-5 
        xl:right-90 
        lg:right-50 
        right-40
        w-4.5 h-4.5 bg-[#FFEFCA] rounded-full"></div>
        <div class="hidden md:block absolute 
            w-[180vw] h-[180vw]
           -top-[35vw] -right-[55vw]

             lg:w-[150vw] lg:h-[150vw]
             lg:-top-[35vw] lg:-right-[45vw]

             xl:w-[120vw] xl:h-[120vw]
             xl:-top-[30vw] xl:-right-[15vw] 
           -translate-x-150   rounded-full border-[10px] border-white/35">
        </div>
        <div class="absolute 
            xl:bottom-10 
            xl:right-98

             lg:bottom-57  
             lg:right-120

             
             bottom-80
             right-88

            w-5 h-5
           bg-[#FFEFCA] rounded-full "></div>
        <div
          class="absolute md:hidden  w-[200vw] h-[200vw] left-1/2 -translate-x-1/2 -bottom-100 
           rounded-full border-[10px] border-amber-50">
        </div>
        <div class="hidden md:block absolute bottom-10 right-150 w-5 h-5 bg-[#FFEFCA] rounded-full "></div>

      </div>
      <Hero />
      <!--Shape scroll-->
      <div class="fixed bottom-0 left-0  w-full">
        <div class="max-w-7xl mx-auto p-6 md:px-12">
          <div class="relative w-10 h-19 
            rounded-full border-4 border-neutral-50
            [mask-image:linear-gradient(to_top,black,transparent)]">
            <div class=" absolute w-6 h-6 animate-bounce bg-white rounded-full top-1/2 left-1 "></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
