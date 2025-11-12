<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import IconIG from '@/Components/Icons/IconIG.vue';
import IconLinkedin from '@/Components/Icons/IconLinkedin.vue';
import IconGithub from '@/Components/Icons/IconGithub.vue';
import IconDiscord from '@/Components/Icons/IconDiscord.vue';
import IconArrow from '@/Components/Icons/IconArrow.vue';
import IconClock from '@/Components/Icons/IconClock.vue';
import IconHome from '@/Components/Icons/IconHome.vue';
import IconUser from '@/Components/Icons/IconUser.vue';
import IconSkill from '@/Components/Icons/IconSkill.vue';

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

// Data untuk My Advantages
const advantages = [
  { name: 'Figma', logo: '/images/logo/Figma-logo.png', percent: '97%' },
  { name: 'VueJS', logo: '/images/logo/Vuejs-logo.png', percent: '70%' },
  { name: 'ReactJS', logo: '/images/logo/React-logo.png', percent: '30%' },
  { name: 'Laravel/PHP', logo: '/images/logo/Laravel-logo.png', percent: '65%' },
  { name: 'JavaScript', logo: '/images/logo/JavaScript-logo.png', percent: '75%' },
];

// Data testimonial
const testimonials = [
  {
    name: 'Bustanil Yasir',
    company: 'CEO of',
    comhig: 'PT. Rupa Raya Indonesia',
    image: '/images/logo/profil.png',
    text: 'Hafizh adalah sosok yang menunjukkan dedikasi dan ketelitian dalam setiap proyek yang ditangani',
  },
  {
    name: 'Ghassan Zakiri',
    company: 'CEO of',
    comhig: 'Need Skill Academy',
    image: '/images/logo/profil3.png',
    text: 'Anak yang idenya out of the box dan suka mengambil resiko, tapi tidak semua pemuda bisa seperti Hafizh',
  },
  {
    name: 'Idris Suyupi',
    company: 'Ketua Jurusan PPLG',
    comhig: 'SMKN 1 Pangkajene dan Kepulauan',
    image: '/images/logo/profil2.png',
    text: 'Ananda Hafizh adalah salah satu siswa terbaik di jurusan PPLG. Ananda menunjukkan semangat belajar yang tinggi serta sikap profesional yang jarang dimiliki di usia muda',
  },
  {
    name: 'Raihan Ali',
    company: 'Alumni Angkatan 2023',
    comhig: 'SMK Telkom Makassar',
    image: '/images/logo/profil2.png',
    text: 'Buat saya, Hafizh itu tipe orang yang tidak banyak bicara tapi hasil kerjanya selalu berbicara',
  },
];

const testimonialIndex = ref(0);

function nextTestimonial() {
  testimonialIndex.value = (testimonialIndex.value + 1) % testimonials.length;
}
function prevTestimonial() {
  testimonialIndex.value =
    (testimonialIndex.value - 1 + testimonials.length) % testimonials.length;
}
</script>
<template>
  <main>
    <section class="max-w-[1440px] mx-auto">
      <div class="grid grid-cols-1 md:grid-cols-[350px_1fr] gap-32 py-10">
        <!-- Sidebar kiri -->
        <aside
          class="text-white py-10 px-8 border border-neutral-700 rounded-3xl space-y-7 h-fit w-full md:w-[350px] mb-8 md:mb-0 md:sticky md:top-10"
        >
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
        <!-- Main konten -->
        <main class="flex flex-col">
            <aside class="fixed right-20 top-1/2 transform -translate-y-1/2 flex flex-col z-50 hidden sm:flex border border-neutral-700 py-4 rounded-full">
                    <a href="#home" title="Clock" class="w-12 h-12 flex items-center justify-center bg-opacity-10 text-white rounded-full hover:bg-opacity-20 transition">
                        <IconHome width="23" height="23" />
                    </a>
                    <a href="#about" title="Instagram" class="w-12 h-12 flex items-center justify-center bg-opacity-10 text-white rounded-full hover:bg-opacity-20 transition">
                        <IconUser width="23" height="23" />
                    </a>
                    <a href="#skill" title="LinkedIn" class="w-12 h-12 flex items-center justify-center bg-opacity-10 text-white rounded-full hover:bg-opacity-20 transition">
                        <IconSkill width="20" height="23" />
                    </a>
                    <a href="#" title="GitHub" class="w-12 h-12 flex items-center justify-center bg-opacity-10 text-white rounded-full hover:bg-opacity-20 transition">
                        <IconGithub width="23" height="23" />
                    </a>
                    <a href="#" title="Discord" class="w-12 h-12 flex items-center justify-center bg-opacity-10 text-white rounded-full hover:bg-opacity-20 transition">
                        <IconDiscord width="23" height="23" />
                    </a>
                </aside>    
          <section id="home" class="flex flex-wrap gap-7 mt-0 md:py-20">
            <div class="space-y-8">
                <div class="flex items-center gap-x-3 border border-neutral-700 rounded-full py-2 px-4 w-fit mb-10">
                    <IconHome width="23" class="text-white" />
                    <p class="text-sm text-neutral-400 tracking-wide">
                        INTRODUCE
                    </p>
                </div>
              <h1 class="sm:text-7xl text-5xl text-white tracking-wide">Say Hi from <span class="text-[#28E98C]">Hafizh</span>, <br>Web Developer <br>and UI Designer</h1>
              <p class="text-neutral-400 tracking-wider">
                Menggabungkan kreativitas dan logika untuk membangun website <br>yang menarik dan mudah digunakan
              </p>
            </div>
          </section>

          <section id="about" class="py-48 flex gap-7">
            <div class="max-w-2xl space-y-8">
                <div class="flex items-center gap-x-3 border border-neutral-700 rounded-full py-2 px-4 w-fit mb-10">
                    <IconUser width="20" class="text-white" />
                    <p class="text-sm text-neutral-400 tracking-wide">
                        ABOUT
                    </p>
                </div>
              <h3 class="text-5xl text-white tracking-wide leading-tight">Every great design begin with an even <span class="text-[#28E98C]">better story</span></h3>
              <p class="text-neutral-400 tracking-wider leading-relaxed">
                Sejak memulai perjalanan sebagai web developer dan UI/UX designer, saya telah terlibat dalam berbagai proyek, mulai dari pengembangan website pribadi, kolaborasi tim, hingga merancang antarmuka untuk kebutuhan bisnis. Saya tipe orang yang tenang namun selalu penasaran, terus belajar hal baru, dan berusaha menyempurnakan setiap detail dalam setiap proyek yang saya kerjakan.
              </p>
            </div>
          </section>

          <section id="skill" class="pt-20 flex gap-7">
            <div class="max-w-3xl space-y-8">
                <div class="flex items-center gap-x-3 border border-neutral-700 rounded-full py-2 px-4 w-fit mb-10">
                    <IconSkill width="20" class="text-white" />
                    <p class="text-sm text-neutral-400 tracking-wide">
                        MY SKILL
                    </p>
                </div>
              <h3 class="text-5xl text-white tracking-wide leading-tight">My <span class="text-[#28E98C]">Advantages</span></h3>
              <div>
                <div class="flex flex-wrap gap-8">
                  <div
                  v-for="(adv, i) in advantages"
                  :key="i"
                  class="flex flex-col items-center"
                  >
                  <div class="border border-neutral-700 hover:border-[#28E98C] duration-300 rounded-full py-12 px-12 flex flex-col items-center">
                    <img :src="adv.logo" alt="" class="w-12">
                    <h4 class="text-3xl tracking-wider text-[#28E98C] mt-5">
                      {{ adv.percent }}
                    </h4>
                  </div>
                  <p class="text-neutral-400 mt-5">
                    {{ adv.name }}
                  </p>
                </div>
              </div>
              </div>
            </div>
          </section>

          <section class="mt-20 flex gap-7">
            <div class="max-w-3xl space-y-8">
              <h3 class="text-5xl text-white tracking-wide leading-tight">Achievement<span class="text-[#28E98C]"> Results</span></h3>
                <div class="flex flex-wrap gap-8">
                  <h6 class="text-white text-2xl">Coming <span class="text-[#28E98C]">Soon..</span></h6>
                </div>
              </div>
          </section>

          <section class="mt-20 flex gap-7">
            <div class="max-w-2xl space-y-8">
              <h3 class="text-5xl text-white tracking-wide leading-tight">
              Trusted by <span class="text-[#28E98C]">Relation</span>
              </h3>
              <div>
              <div class="flex flex-wrap gap-8 items-center">
                <transition name="fade" mode="out-in">
                <div
                  :key="testimonialIndex"
                  class="border border-neutral-700 rounded-3xl py-12 px-12 w-full"
                >
                  <div class="flex gap-x-5 items-center">
                  <img :src="testimonials[testimonialIndex].image" alt="" class="object-top w-14 h-14 rounded-full">
                  <div>
                    <h5 class="tracking-wide text-lg text-white">
                    {{ testimonials[testimonialIndex].name }}
                    </h5>
                    <p class="text-neutral-400">
                    {{ testimonials[testimonialIndex].company }} <span class="text-[#28E98C]">{{ testimonials[testimonialIndex].comhig }}</span>
                    </p>
                  </div>
                  </div>
                  <p class="text-neutral-200 text-2xl mt-5 tracking-wide">
                  {{ testimonials[testimonialIndex].text }}
                  </p>
                </div>
                </transition>
              </div>
              <div class="flex items-center mt-8 gap-4">
                <button
                @click="prevTestimonial"
                class="border border-neutral-700 rounded-full px-4 py-2 text-white hover:border-[#28E98C] duration-300"
                >
                ‹
                </button>
                <span class="text-white font-semibold text-lg select-none">
                {{ testimonialIndex + 1 }} / {{ testimonials.length }}
                </span>
                <button
                @click="nextTestimonial"
                class="border border-neutral-700 rounded-full px-4 py-2 text-white hover:border-[#28E98C] duration-300"
                >
                ›
                </button>
              </div>
              </div>
            </div>
          </section>
        </main>
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

.fade-enter-active, .fade-leave-active {
  transition: opacity 0.4s cubic-bezier(.4,0,.2,1);
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
.fade-enter-to, .fade-leave-from {
  opacity: 1;
}
</style>