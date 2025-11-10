<script setup>
import IconIG from '@/Components/Icons/IconIG.vue';
import IconLinkedin from '@/Components/Icons/IconLinkedin.vue';
import IconGithub from '@/Components/Icons/IconGithub.vue';
import IconDiscord from '@/Components/Icons/IconDiscord.vue';
import IconArrow from '@/Components/Icons/IconArrow.vue';
import IconClock from '@/Components/Icons/IconClock.vue';
</script>
<template>
    <main>
        <section class="max-w-[1440px] mx-auto">

            <main class="grid grid-cols-[380px_1fr] items-start gap-48 py-10">
                <aside class="text-white py-10 px-8 border border-neutral-700 rounded-3xl space-y-7 sticky top-10 h-fit">
                    <div class="grid grid-cols-2 items-center justify-around">
                        <img src="/images/FOLIO..png" class="w-28" alt="">
                        <h3 class="text-right text-sm">
                            Web Developer <br>& UI/UX Designer
                        </h3>
                    </div>
                    <div class="flex justify-center">
                        <img src="/images/model.jpg" class="object-cover w-60 rounded-3xl" alt="">
                    </div>
                    <h1 class="text-2xl text-center pt-5">
                        Muhammad Hafizh <br>Based in Makassar, IND
                    </h1>
                    <p class="text-neutral-400 font-medium text-center">
                        © 2025 Folio. All Rights Reserved
                    </p>
                    <div class="flex gap-x-3 justify-center">
                        <a href="#"><IconIG width="40" height="40" class="bg-white bg-opacity-10 text-white p-2 rounded-full"/></a>
                        <a href="#"><IconLinkedin width="40" height="40" class="bg-white bg-opacity-10 text-white p-2 rounded-full"/></a>
                        <a href="#"><IconGithub width="40" height="40" class="bg-white bg-opacity-10 text-white p-2 rounded-full"/></a>
                        <a href="#"><IconDiscord width="40" height="40" class="bg-white bg-opacity-10 text-white p-2 rounded-full"/></a>
                    </div>
                    <a href="" class="group relative overflow-hidden flex justify-center w-full gap-x-2 border border-[#28E98C] bg-[#28E98C] px-8 py-4 rounded-full text-md font-medium transition-none">
                        <span class="relative z-10 text-[#181818] transition-colors duration-300">Let's Talk</span>
                        <IconArrow icon="majesticons:arrow-up-line" class="text-black rotate-45 group-hover:rotate-90 duration-300 relative z-10" />
                    </a>
                </aside>

                <aside class="fixed right-20 top-1/2 transform -translate-y-1/2 flex flex-col z-50 hidden sm:flex border border-neutral-700 py-4 rounded-full">
                    <a href="#" title="Clock" class="w-12 h-12 flex items-center justify-center bg-opacity-10 text-white rounded-full hover:bg-opacity-20 transition">
                        <IconClock width="23" height="23" />
                    </a>
                    <a href="#" title="Instagram" class="w-12 h-12 flex items-center justify-center bg-opacity-10 text-white rounded-full hover:bg-opacity-20 transition">
                        <IconIG width="23" height="23" />
                    </a>
                    <a href="#" title="LinkedIn" class="w-12 h-12 flex items-center justify-center bg-opacity-10 text-white rounded-full hover:bg-opacity-20 transition">
                        <IconLinkedin width="23" height="23" />
                    </a>
                    <a href="#" title="GitHub" class="w-12 h-12 flex items-center justify-center bg-opacity-10 text-white rounded-full hover:bg-opacity-20 transition">
                        <IconGithub width="23" height="23" />
                    </a>
                    <a href="#" title="Discord" class="w-12 h-12 flex items-center justify-center bg-opacity-10 text-white rounded-full hover:bg-opacity-20 transition">
                        <IconDiscord width="23" height="23" />
                    </a>
                </aside>

                <main class="flex flex-col mt-40">
                    <section class="flex flex-wrap gap-7">
                        <div class="space-y-8">
                            <h1 class="text-7xl text-white font-extralight tracking-wide leading-none">Say Hi from <span class="text-[#28E98C]">Hafizh</span>, <br>Web Developer <br>and UI Designer</h1>
                            <p class="text-neutral-400 tracking-wider">
                                Menggabungkan kreativitas dan logika untuk membangun website <br>yang menarik dan mudah digunakan
                            </p>
                            <!-- <div class="flex flex-wrap sm:justify-start justify-center gap-5 items-center">
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
                            </div> -->
                        </div>
                    </section>
                    <section class="mt-80 flex gap-7">
                        <div class="max-w-2xl space-y-8">
                            <h3 class="text-5xl text-white font-extralight tracking-wide leading-tight">Every great design begin with an even better story</h3>
                            <p class="text-neutral-400 tracking-wider">
                                Seseorang yang berfokus pada pengembangan web dan desain antarmuka pengguna. Ketelitian dalam detail, konsistensi visual, dan pengalaman pengguna yang intuitif menjadi prioritas utama dalam setiap proyek yang saya kerjakan. Bagi saya, sebuah website yang baik adalah perpaduan antara fungsi, estetika, dan kemudahan penggunaan.
                            </p>
                            <!-- <div class="flex flex-wrap sm:justify-start justify-center gap-5 items-center">
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
                            </div> -->
                        </div>
                    </section>
                </main>
            </main>


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
</style>