<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import IconIG from '@/Components/Icons/IconIG.vue';
import IconLinkedin from '@/Components/Icons/IconLinkedin.vue';
import IconGithub from '@/Components/Icons/IconGithub.vue';
import IconDiscord from '@/Components/Icons/IconDiscord.vue';
import IconArrow from '@/Components/Icons/IconArrow.vue';
import IconClock from '@/Components/Icons/IconClock.vue';

const timeWITA = ref('');

function updateTime() {
    const now = new Date();

    const utc = now.getTime() + (now.getTimezoneOffset() * 60000);
    const wita = new Date(utc + (8 * 60 * 60 * 1000));

    const hours = wita.getHours().toString().padStart(2, '0');
    const minutes = wita.getMinutes().toString().padStart(2, '0');
    timeWITA.value = `${hours}.${minutes}`;
}

let intervalId;
onMounted(() => {
    updateTime();
    intervalId = setInterval(updateTime, 1000);
});
onUnmounted(() => {
    clearInterval(intervalId);
});
</script>

<template>
    <main>
        <nav class="border-b border-neutral-800">
            <div class="max-w-[1220px] mx-auto px-5 py-8">
                <div class="flex justify-between items-center">
                    <img src="/images/FOLIO..png" class="w-28" alt="">
                    <div class="flex items-center text-neutral-100 gap-8 font-semibold">
                        <a href="/">Home</a>
                        <a href="#">About Us</a>
                        <a href="#">Contact Me</a>
                    </div>
                    <div class="flex gap-x-3 items-center">
                        <IconClock icon="flowbite:clock-solid" width="24" height="24" class="text-neutral-100" />
                        <span class="text-neutral-500 text-sm font-medium">{{ timeWITA }}</span>
                    </div>
                </div>
            </div>
        </nav>

        <section class="max-w-[1220px] mx-auto px-5 flex flex-col gap-y-10 justify-center">
            <div class="text-white space-y-5 mt-20">
                <div class="max-w-fit mx-auto border border-[#28E98C] px-8 py-1 rounded-full">
                    <h3 class="text-[#28E98C] text-center">Hi, I’m Muhammad Hafizh</h3>
                </div>
                <h1 class="sm:text-7xl text-3xl font-medium text-center">Build Ideas Into Impactful <br>Digital Experiences</h1>
            </div>
            <div class="flex flex-wrap items-center gap-7 justify-center">
                <div class="max-w-lg space-y-8">
                    <p class="text-lg sm:text-start text-center font-medium text-neutral-500 tracking-wide">Loves turning creative concepts into clean, functional, and user-friendly websites. Whether it’s frontend or full-stack development, I enjoy crafting solutions that bring real value to people.</p>
                    <div class="flex flex-wrap sm:justify-start justify-center gap-5 items-center">
                        <a href="" class="group relative overflow-hidden flex w-fit gap-x-2 border border-[#28E98C] bg-[#28E98C] px-8 py-4 rounded-full text-md font-medium transition-none">
                            <span class="relative z-10 text-[#181818] transition-colors duration-300">Let's Talk</span>
                            <IconArrow icon="majesticons:arrow-up-line" class="rotate-45 group-hover:rotate-90 duration-300 relative z-10" />
                        </a>
                        <div class="flex gap-x-3">
                            <a href="#"><IconIG width="40" height="40" class="bg-white bg-opacity-10 text-white p-2 rounded-full"/></a>
                            <a href="#"><IconLinkedin width="40" height="40" class="bg-white bg-opacity-10 text-white p-2 rounded-full"/></a>
                            <a href="#"><IconGithub width="40" height="40" class="bg-white bg-opacity-10 text-white p-2 rounded-full"/></a>
                            <a href="#"><IconDiscord width="40" height="40" class="bg-white bg-opacity-10 text-white p-2 rounded-full"/></a>
                        </div>
                    </div>
                </div>
                <div>
                    <img src="/images/actrr.png" class="object-cover w-60 h-80 object-top" alt="">
                </div>
                <div class="sm:block max-w-xs hidden space-y-2 border border-neutral-700 px-5 py-4 rounded-xl">
                    <h1 class="text-2xl text-gray-200">My Tech Stacks</h1>
                    <p class="text-md text-gray-300">Expert in modern tech stacks: <br>VueJS, Laravel, Flutter, Figma, and more.</p>
                </div>
            </div>
        </section>

        <section class="bg-white">
            <div class="max-w-[1220px] flex flex-wrap gap-y-8 justify-around items-center mx-auto px-5 py-20">
                <div class="relative">
                    <div class="absolute -top-5 -right-5 w-32 h-32 bg-[#28E98C] bg-opacity-50 rounded-xl animate-bounce delay-300"></div>
                    <img src="/images/modell.jpg" class="object-cover w-[34em] h-[26em] rounded-tl-[9em] rounded-br-[9em] rounded-bl-xl rounded-tr-xl shadow-2xl" alt="">
                    <div class="absolute -bottom-5 -left-5 w-32 h-64 bg-[#28E98C] bg-opacity-50 rounded-xl animate-bounce"></div>
                </div>
                <div class="max-w-lg space-y-5">
                    <h1 class="text-5xl text-neutral-900 font-medium">My Story and Expertise</h1>
                    <p class="text-base font-medium text-neutral-500 tracking-wide">With a strong interest in web technologies and user interface design, I specialize in front-end development using Vue.js, TailwindCSS, and more. I also have hands-on experience with PHP, enabling me to build responsive and visually consistent websites.</p>
                    <div class="flex flex-wrap gap-x-5">
                        <!-- button 2 -->
                        <a href="" class="group relative overflow-hidden flex w-fit gap-x-2 border bg-[#28E98C] px-8 py-4 rounded-full text-md font-medium transition-none">
                            <span class="relative z-10 text-[#181818] group-hover:text-white transition-colors duration-300">Let's Talk</span>
                            <IconArrow icon="majesticons:arrow-up-line" class="rotate-45 group-hover:text-white group-hover:rotate-90 duration-300 relative z-10" />
                        </a>
                        <!-- button 3 -->
                        <!-- <a href="" class="group relative overflow-hidden flex w-fit gap-x-2 border border-neutral-800 bg-transparent px-8 py-4 rounded-full text-md font-medium transition-none">
                            <span class="relative z-10 text-neutral-800 group-hover:text-white transition-colors duration-300">Let's Talk</span>
                            <IconArrow icon="majesticons:arrow-up-line" class="rotate-45 group-hover:text-white group-hover:rotate-90 duration-300 relative z-10" />
                        </a> -->
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-white">
            <div class="max-w-[1220px] flex flex-wrap gap-y-8 justify-around items-center mx-auto px-5 py-20">
                <div class="relative">
                    <h1 class="text-9xl font-semibold text-center">If You Know <br> Then You Know</h1>
                </div>
            </div>
        </section>

        <section class="bg-white">
            <div class="max-w-[1220px] flex flex-wrap gap-y-8 justify-around items-center mx-auto px-5 py-20">
                <div class="relative">
                </div>
            </div>
        </section>

        
    </main>
</template>

<style scoped>
a.group {
  position: relative;
  overflow: hidden;
}

/* Button 1: border-[#28E98C] bg-[#28E98C] (hover putih) */
a.border-\[\#28E98C\].bg-\[\#28E98C\]::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  width: 0%;
  height: 100%;
  background: #fff;
  border-radius: 9999px;
  transition: width 0.5s cubic-bezier(.4,0,.2,1);
  z-index: 1;
}
a.border-\[\#28E98C\].bg-\[\#28E98C\]:hover::before {
  width: 100%;
}

/* Button 2: bg-[#28E98C] tanpa border-[#28E98C] (hover #1C1D20) */
a.bg-\[\#28E98C\]:not(.border-\[\#28E98C\])::before,
a.border-neutral-800.bg-transparent::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  width: 0%;
  height: 100%;
  background: #1C1D20;
  border-radius: 9999px;
  transition: width 0.5s cubic-bezier(.4,0,.2,1);
  z-index: 1;
}
a.bg-\[\#28E98C\]:not(.border-\[\#28E98C\]):hover::before,
a.border-neutral-800.bg-transparent:hover::before {
  width: 100%;
}

a.group .z-10 {
  position: relative;
  z-index: 10;
}

@keyframes bounce {
    0%, 100% {
        transform: translateY(-5%);
        animation-timing-function: cubic-bezier(0.8,0,1,1);
    }
    50% {
        transform: none;
        animation-timing-function: cubic-bezier(0,0,0.2,1);
    }
}
.animate-bounce {
    animation: bounce 3s infinite;
}
</style>