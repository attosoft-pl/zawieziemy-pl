<template>
  <div id="footer" class="dark:bg-[#262523] dark:text-[#C7C7C4] lg:max-w-[1024px] mx-auto">
    <section class="md:flex">
      <!--  -->
      <div class="flex flex-col flex-1 shrink basis-0 min-w-[193px] max-md:max-w-full">
        <div class="flex gap-2 items-center max-w-full text-2xl text-white whitespace-nowrap min-h-[48px] w-[193px]">
          <img
            src="./assets/images/logo-tex-S.svg"
            class="object-contain shrink-0 self-stretch my-auto" alt="Logo ZawiezieMy" />
          <div class="self-stretch my-auto sr-only">ZawiezieMy</div>
        </div>
        <div class="mt-6 text-base font-semibold text-stone-300 max-md:max-w-full- max-w-[100vw]">
          <span>
            Naszym priorytetem jest Twoje bezpieczeństwo i komfort. Stawiamy na indywidualne podejście, dostosowując się
            do Twoich potrzeb.
          </span>
          <br /><br />
          <span class="font-bold">Ty wyznaczasz cel, my znajdziemy najlepszą drogę.</span>
        </div>
      </div>
      <!--  -->
      <div class="flex flex-col flex-1 shrink basis-0 min-w-[207px]">
        <div class="shrink gap-2.5 w-full text-xl font-bold whitespace-nowrap text-stone-300">
          Kontakt
        </div>
        <div class="flex flex-col mt-6 w-full text-sm font-semibold text-yellow-400">
          <div class="flex gap-2 w-full text-stone-300">
            <img
              src="./assets/images/phone.svg"
              class="object-contain shrink-0 self-start w-6 aspect-square" alt="24/7 Icon" />
            <div class="flex-1 shrink basis-0">Dostępność 24/7</div>
          </div>
          <div class="flex gap-2 mt-3 w-full">
            <img
              src="./assets/images/phone.svg"
              class="object-contain shrink-0 self-start w-6 aspect-square" alt="Phone Icon" />
            <a href="tel://+48538538757" class="flex-1 shrink basis-0">
              (+ 48) 538-538-757
            </a>
          </div>
          <div class="flex gap-2 mt-3 w-full whitespace-nowrap">
            <img
              src="./assets/images/mail.svg"
              class="object-contain shrink-0 self-start w-6 aspect-square" alt="Email Icon" />
            <a href="mailto://zawieziemypl@gmail.com" class="flex-1 shrink basis-0">zawieziemypl@gmail.com</a>
          </div>
          <div class="flex gap-2 mt-3 w-full whitespace-nowrap">
            <img
              src="./assets/images/msg.svg"
              class="object-contain shrink-0 self-start w-6 aspect-square" alt="Messenger Icon" />
            <a href="https://m.me/zawieziemypl" class="flex-1 shrink basis-0">m.me/zawieziemypl</a>
          </div>
        </div>
      </div>
      <!--  -->
      <div class="flex flex-col flex-1 shrink basis-0 min-w-[207px]">
        <div class="text-xl font-bold text-stone-300">
          Śledź nas w social mediach
        </div>
        <div class="flex flex-wrap gap-6 items-center self-start mt-6">
          <a v-for="(icon, index) in socialIcons" :key="index" :href="icon.link" target="_blank">
          <img :src="icon.src" :alt="icon.alt"
            class="object-contain shrink-0 self-stretch my-auto w-8 aspect-square" />
          </a>
        </div>
      </div>
    </section>
    <section id="veryfooter">
      <div class="flex flex-col">
        <div class="flex w-full bg-stone-500 min-h-[1px] max-md:max-w-full"></div>
        <div
          class="flex gap-6 justify-center items-center py-3 w-full text-sm font-semibold text-stone-400 max-md:max-w-full">
          <div class="flex flex-wrap gap-6 items-center self-stretch my-auto min-w-[240px] w-[1152px]">
            <div class="self-stretch my-auto">Copyright © {{currentYear}}</div>
            <div class="self-stretch my-auto" @click.prevent="window.privPol.showModal()">Polityka prywatności</div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
  ({
    template: '#x-footer',
    data() {
      return {
        window,
        socialIcons: [{
            src: './assets/images/icon-fb.svg',
            alt: 'Facebook Icon',
            link: 'https://www.facebook.com/zawieziemypl/',
          },
          {
            src: './assets/images/icon-instagram.svg',
            alt: 'Instagram Icon',
            link: 'https://www.instagram.com/zawieziemy/',
          },
          {
            src: './assets/images/icon-tiktok.svg',
            alt: 'Tiktok Icon',
            link: 'https://www.tiktok.com/@zawieziemy.pl',
          }
        ]
      }
    },
    computed: {
      currentYear() {
        return new Date().getFullYear()
      }
    }
  })
</script>