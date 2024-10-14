<template>
  <div class="mx-auto [&>div>section]:my-[80px]">
    <div class="header bg-[#F8CE08] h-[48px] hidden md:block">
      <div class="lg:max-w-[1024px] mx-auto text-black flex justify-between h-full items-center">
        <div class="left flex text-sm">
          <img class="mr-2" src="../assets/images/phone.svg" alt="phone" />
          <a class="mr-5" href="tel://0048538538757">
            <span> (+48)&nbsp;538&nbsp;538&nbsp;757 </span>
          </a>
          <img class="mr-2" src="../assets/images/mail.svg" alt="mail" />
          <a class="mr-5" href="mailto://zawieziemy.pl@gmail.com">zawieziemy.pl@gmail.com</a>
          <img class="mr-2" src="../assets/images/msg.svg" alt="msg" />
          <a class="mr-5" href="https://m.me/zawieziemypl">m.me/zawieziemypl</a>
        </div>
        <div class="right flex">
          <img class="mr-3" src="../assets/images/icon-fb.svg" alt="msg" />
          <img class="mr-3" src="../assets/images/icon-tiktok.svg" alt="msg" />
          <img src="../assets/images/icon-instagram.svg" alt="msg" />
        </div>
      </div>
    </div>
    <nav class="menu flex lg:max-w-[1024px] mx-auto flex justify-between items-center h-[96px]">
      <div class="logo flex-1">
        <img class="mr-2" src="../assets/images/logo-tex-S.svg" alt="logo" />
      </div>
      <button @click="changeVisibility()" class="inline-flex items-center p-2 justify-center md:hidden">
        <span class="sr-only">Open main menu</span>
        <img class="mr-2" src="../assets/images/navi.svg" alt="navi" />
      </button>
      <div :class="{ mobile: isMobileMenuOpen }" class="right hidden md:block font-bold flex underline-offset-4">
        <a href="#home" class="mr-8" :class="{
          'text-white underline decoration-[#F8CE08]': page == 0,
        }" @click.prevent="page = 0">Home</a>
        <a href="#about" class="mr-8" :class="{
          'text-white underline decoration-[#F8CE08]': page == 1,
        }" @click.prevent="page = 1">O nas</a>
        <a href="#kontakt" :class="{
          'text-white underline decoration-[#F8CE08]': page == 2,
        }" @click.prevent="page = 2">Kontakt</a>
      </div>
    </nav>
    <!-- Home page start -->
    <div v-if="page == 0" class="lg:max-w-[1024px] mx-auto">
      <section id="hero" class="grid lg:grid-cols-2 gap-4 grid-flow-col auto-cols-max">
        <div class="max-w-[370px]">
          <div class="text-3xl font-bold text-white">
            <h1>
              ZawiezieMy…<br />
              Ciebie,<br />
              Twoje auto<br />
              i Twoje rzeczy!
            </h1>
          </div>
          <div class="small my-5">
            Naszym priorytetem jest Twoje bezpieczeństwo i komfort.
            Stawiamy na indywidualne podejście, dostosowując się do
            Twoich potrzeb.
          </div>
          <div class="flex flex-col">
            <a class="bg-[#F8CE08] text-black py-2 px-4 rounded text-center flex justify-center mb-3"
              href="tel://0048538538757">
              Zadzwoń
            </a>
            <a class="bg-[#46443B] text-white py-2 px-4 rounded text-center flex justify-center">
              Zapoznaj się z ofertą
            </a>
          </div>
        </div>
        <div class="">
          <div class="hidden lg:flex w-full items-center justify-center">
            <div class="flex transition-all">
              <div v-for="(slide, index) in carSlides" :key="index" :class="[
                'w-[130px] h-[350px] flex-shrink-0 transition-all',
                { 'w-[400px]': currentIndex === index },
              ]" @click="slideTo(index)">
                <img :src="slide.src" :alt="slide.alt" class="w-full h-full object-cover rounded-3xl" />
              </div>
            </div>
          </div>
        </div>
      </section>
      <section id="oferta">
        <div class="title">
          <div class="text-xs text-bold font-bold tracking-widest text-[#A2A19D] text-[#A2A19D] uppercase">
            Oferta
          </div>
          <img class="ml-2" src="../assets/images/Ornament.svg" alt="spacer" />
        </div>
        <h2 class="text-3xl font-bold text-white mt-4 mb-7">
          Ty wyznaczasz cel, my znajdziemy najlepszą drogę.
        </h2>
        <div>
          <ul class="hover:[&>*]:list-disc md:columns-2 text-sm font-semibold">
            <li class="flex items-start">
              <img class="mr-2" src="../assets/images/icon-check.svg" alt="check" />
              Usługi na terenie Bełchatowa i okolicy, w całej Polsce
              oraz zagranicą
            </li>
            <li class="flex items-start">
              <img class="mr-2" src="../assets/images/icon-check.svg" alt="check" />Gwarancja wygody i punktualności
            </li>
            <li class="flex items-start">
              <img class="mr-2" src="../assets/images/icon-check.svg" alt="check" />Dostępność 24/7
            </li>
            <li class="flex items-start">
              <img class="mr-2" src="../assets/images/icon-check.svg" alt="check" />Komfort i bezpieczeństwo
            </li>
            <li class="flex items-start">
              <img class="mr-2" src="../assets/images/icon-check.svg" alt="check" />Idealne na codzienne dojazdy,
              specjalne okazje i pilne
              potrzeby
            </li>
          </ul>
        </div>
        <div class="grid lg:grid-cols-4 md:grid-cols-2 gap-4 items-stretch place-content-center mt-5">
          <div class="flex justify-center" :key="index" v-for="(offer, index) in offersInfo">
            <div class="bg-[#262523] rounded-xl p-4 text-center w-[250px] h-[450px]">
              <div class="flex justify-center items-center mb-4 h-[150px]">
                <div class="w-[128px] flex items-center justify-center">
                  <img class="mr-2" :src="offer.src" alt="oferta-icon" />
                </div>
              </div>
              <div class="text-white text-lg font-bold">
                {{ offer.title }}
              </div>
              <ul class="text-[#A2A19D] text-sm mt-3 space-y-1 text-left">
                <li v-for="(point, index2) in offer.points" :key="index2" class="flex items-start">
                  <img src="../assets/images/iron-dot-S.svg" alt="dot" />{{ point }}
                </li>
              </ul>
            </div>
          </div>
        </div>
      </section>
      <section id="opinie">
        <div class="title">
          <div class="text-xs text-bold font-bold tracking-widest text-[#A2A19D] uppercase">
            Opinie
          </div>
          <img class="ml-2" src="../assets/images/Ornament.svg" alt="spacer" />
        </div>
        <h2 class="text-3xl font-bold text-white mt-4 mb-7">
          Nie wierz nam na słowo, sprawdź co mówią o nas inni.
        </h2>
        <div class="w-full mx-auto overflow-hidden">
          <div class="flex transition-transform duration-300 ease-out lg:gap-4" :style="{
            transform: `translateX(-${(activeSlide * 100) / visibleSlides
              }%)`,
          }">
            <div v-for="(slide, index) in slides" :key="index" class="w-full lg:w-1/3 flex-shrink-0">
              <div class="bg-[#262523] p-4 rounded-lg shadow-lg text-[#A2A19D] lg:h-60">
                <img src="../assets/images/Quote.svg" alt="quote" />
                <p class="text-base font-bold my-6 mr-3">{{ slide.quote }}</p>
                <p class="text-sm font-semibold mb-1">
                  {{ slide.name }}
                </p>
                <p class="text-xs">{{ slide.source }}</p>
              </div>
            </div>
          </div>
          <div class="flex justify-center items-center relative min-h-7 my-2">
            <span v-for="(_dot, index) in totalDots" :key="index" class="h-2 w-2 mx-1 rounded-full cursor-pointer"
              :class="{
                'bg-white': index === activeSlide,
                'bg-gray-500': index !== activeSlide,
              }" @click="setActiveSlide(index)"></span>

            <button @click="prevSlide" class="absolute left-0">
              <img src="../assets/images/icon-arrow-simple-left.svg" alt="arrow-left" />
            </button>
            <button @click="nextSlide" class="absolute right-0">
              <img src="../assets/images/icon-arrow-simple-right.svg" alt="arrow-right" />
            </button>
          </div>
        </div>
      </section>
      <section id="map" @click="(map += 1), (map %= 4)">
        <div class="title">
          <div class="text-xs text-bold font-bold tracking-widest text-[#A2A19D] uppercase">
            Mapa
          </div>
          <img class="ml-2" src="../assets/images/Ornament.svg" alt="spacer" />
        </div>
        <!-- <button @click="map += 1, map %= 4">dalej</button> -->
        <div class="relative mt-5">
          <div class="absolute top-[41px] left-[35px]">
            <div class="flex flex-col md:flex-row space-x-2 text-xs font-semibold">
              <button @click="setActiveButton(0)" :class="{
                'bg-[#F8CE08] text-[#22211F]': 0 === activeButton,
                'bg-[#666562] text-white': 0 !== activeButton,
              }" class="px-4 py-2 h-[32px] rounded-full text-center flex justify-center">
                Usługi taxi
              </button>
              <button @click="setActiveButton(1)" :class="{
                'bg-[#F8CE08] text-[#22211F]': 1 === activeButton,
                'bg-[#666562] text-white': 1 !== activeButton,
              }" class="px-4 py-2 h-[32px] rounded-full text-center flex justify-center">
                Przewóz busem
              </button>
              <button @click="setActiveButton(2)" :class="{
                'bg-[#F8CE08] text-[#22211F]': 2 === activeButton,
                'bg-[#666562] text-white': 2 !== activeButton,
              }" class="px-4 py-2 h-[32px] rounded-full text-center flex justify-center">
                Pomoc drogowa
              </button>
              <button @click="setActiveButton(3)" :class="{
                'bg-[#F8CE08] text-[#22211F]': 3 === activeButton,
                'bg-[#666562] text-white': 3 !== activeButton,
              }" class="px-4 py-2 h-[32px] rounded-full text-center flex justify-center">
                Autoholowanie
              </button>
            </div>
          </div>
          <div v-show="activeButton === 0" contenteditable="false">
            <img src="../assets/images/taxi.png" />
          </div>
          <div v-show="activeButton === 1" contenteditable="false">
            <img src="../assets/images/bus.png" />
          </div>
          <div v-show="activeButton === 2" contenteditable="false">
            <img src="../assets/images/pomo.png" />
          </div>
          <div v-show="activeButton === 3" contenteditable="false">
            <img src="../assets/images/holowanie.png" />
          </div>
        </div>
      </section>
    </div>
    <!-- Home page end -->
    <!-- About start -->
    <div v-show="page == 1">
      <div class="flex">
        <div class="flex-1">
          <h2>Zaufaj naszemu doświadczeniu</h2>
          <p>
            Firma zawieziemy powstała w 2023 r. Jednak z transportem
            jesteśmy związani od kilku lat. Przez ten okres zdobyliśmy
            spore doświadczenie przede wszystkim na trasach
            międzynarodowych.
          </p>
          <p>
            Dzięki bogatemu doświadczeniu możemy świadczyć usługi na
            najwyższym poziomie, dbając o satysfakcję oraz
            bezpieczeństwo naszych klientów – zarówno tych obecnych,
            jak i nowych.
          </p>
          <p>
            Działamy głównie w Bełchatowie i okolicach, ale
            obsługujemy również zlecenia na terenie całego kraju oraz
            poza jego granicami.
          </p>
        </div>
        <div class="flex-1">
          <img src="./about-col-2nd.png" alt="" />
        </div>
      </div>
    </div>
    <!-- About end -->
    <!-- Kontakt start -->
    <div v-show="page == 2">
      <div class="flex max-w-full">
        <div class="flex-1">
          <img src="./contact-col-1st.png" alt="" />
        </div>
        <div class="flex-1">
          <img src="./contact-col-2nd.png" alt="" />
        </div>
      </div>
    </div>
    <!-- Kontakt end -->
    <section id="footer" class="dark:bg-[#262523] dark:text-[#C7C7C4]">
      <div contenteditable="false">
        <img src="./footer-mock.png" alt="" />
      </div>
      <hr />
      <div>
        <span> Copyright &copy; 2024 </span>
        <a href="#" @click.prevent="window.privPol.showModal()">Polityka prywatności</a>
      </div>
    </section>
    <dialog id="privPol">
      <form method="dialog">
        <button type="submit">x</button>
      </form>
      <h1>Polityka prywatności</h1>
      <p>Nasz polityka prywatności to...</p>
    </dialog>
  </div>
</template>

<script>
new Vue({
  components: {},
  template: '#x-app',
  el: '#app',
  data() {
    return {
      isDev: localStorage.isDev,
      // ...{isDev}: localStorage,
      window,
      map: 0,
      page: ['#home', '#about', '#kontakt'].indexOf(location.hash),
      page: {
        [location.hash]: 0,
        '#home': 0,
        '#about': 1,
        '#kontakt': 2,
      }[location.hash],
      isMobileMenuOpen: false,
      currentIndex: 0,
      carSlides: [
        {
          src: '../assets/images/car_1.png',
          alt: 'Pomoc drogowa Bełchatów',
        },
        {
          src: '../assets/images/car_2.png',
          alt: 'Przewóz osób Bełchatów',
        },
        {
          src: '../assets/images/car_3.png',
          alt: 'Taxi Bełchatów, car, roof',
        },
      ],
      offersInfo: [
        {
          src: '../assets/images/icon-oferta.svg',
          title: 'Usługi taxi',
          points: [
            'przewóz do 4 osób',
            'szybki czas realizacji',
            'nocne przewozy – bezpieczny powrót do domu po imrezach',
            'przejazdy do pracy i z pracy',
            'duży bagażnik',
            'przewozimy na terenie całej Polski (z i do Bełchatowa)',
          ],
        },
        {
          src: '../assets/images/icon-oferta_2.svg',
          title: 'Przewóz osób busem',
          points: [
            'przewóz do 8 osób',
            'przyjęcia okolicznościowe (wesela, komunie i inne imprezy rodzinne)',
            'wieczory kawalerskie i panieńskie, dyskoteki i inne',
            'transfery na lotniska i dworce',
            'cała Polska i zagranica',
          ],
        },
        {
          src: '../assets/images/icon-oferta_3.svg',
          title: 'Pomoc drogowa',
          points: [
            'awaryjne odpalanie pojazdu',
            'dowóz paliwa',
            'pomoc na miejscu po awarii',
            'wymiana koła',
            'Bełchatów i okolice, trasy A1, A2, S8 i DK74',
          ],
        },
        {
          src: '../assets/images/icon-oferta_4.svg',
          title: 'Autoholowanie',
          points: [
            'pojazdy sprawne, uszkodzone i powypadkowe',
            'pomoc po kolizji drogowej',
            'pojazdy do 1,5 tony',
            'przewóz do 2 osób',
            'na terenie całej Polski',
          ],
        },
      ],
      activeSlide: 0,
      slides: [
        {
          quote:
            'Polecam, profesjonalne podejście, szybka reakcja, samochód mimo ciężkich warunków wyciągnięty od razu.',
          name: 'Marysia Ch.',
          source: 'via. Facebook',
        },
        {
          quote:
            'Polecam! Człowiek godny zaufania i polecania. Bezproblemowo przyjechał po auto w środku nocy w weekend!',
          name: 'Rafał',
          source: 'via. Google',
        },
        {
          quote:
            'Profesjonalne usługi, przystępne i konkurencyjne ceny, sprawne i szybkie działanie 24/7. Polecam w 100%!',
          name: 'Angelina S.',
          source: 'via. Google',
        },
        {
          quote:
            'Profesjonalne usługi, przystępne i konkurencyjne ceny, sprawne i szybkie działanie 24/7. Polecam w 100%!',
          name: 'Artur D.',
          source: 'via. Google',
        },
        {
          quote:
            'Profesjonalne usługi, przystępne i konkurencyjne ceny, sprawne i szybkie działanie 24/7. Polecam w 100%!',
          name: 'Sara T.',
          source: 'via. Google',
        },
        {
          quote:
            'Profesjonalne usługi, przystępne i konkurencyjne ceny, sprawne i szybkie działanie 24/7. Polecam w 100%!',
          name: 'Kuba B.',
          source: 'via. Google',
        },
      ],
      windowWidth: window.innerWidth,
      activeButton: 0
    };
  },

  methods: {
    changeVisibility() {
      this.isMobileMenuOpen = !this.isMobileMenuOpen;
    },
    slideTo(index) {
      this.currentIndex = index;
    },
    setActiveSlide(index) {
      this.activeSlide = index;
    },
    prevSlide() {
      if (this.activeSlide > 0) {
        this.activeSlide--;
      } else {
        this.activeSlide = this.totalDots - 1;
      }
    },
    nextSlide() {
      if (this.activeSlide < this.totalDots - 1) {
        this.activeSlide++;
      } else {
        this.activeSlide = 0;
      }
    },
    handleResize() {
      this.windowWidth = window.innerWidth;
      if (this.activeSlide >= this.totalDots) {
        this.activeSlide = this.totalDots - 1;
      }
    },
    setActiveButton(button) {
      this.activeButton = button;
    },
  },

  computed: {
    visibleSlides() {
      return this.windowWidth >= 1024 ? 3 : 1;
    },
    totalDots() {
      return Math.ceil(this.slides.length / this.visibleSlides);
    },
  },

  watch: {
    page(v) {
      location.hash = ['home', 'about', 'kontakt'][v];
    },
  },

  mounted() {
    window.addEventListener('resize', this.handleResize);
  },

  beforeDestroy() {
    window.removeEventListener('resize', this.handleResize);
  },
});
</script>
