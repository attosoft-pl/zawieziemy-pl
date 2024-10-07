<template>
  <div class="mx-auto [&>div>section]:my-[20px] [&>div>section]:border [&>div>section]:border-black">
    <div class="header bg-[#F8CE08] h-[48px] hidden md:block">
      <div class="lg:max-w-[1024px] mx-auto text-black flex justify-between h-full items-center">
        <div class="left flex text-sm">
          <img class="mr-2" src="../assets/images/phone.svg" alt="phone">
          <a class="mr-5" href="tel://0048538538757">
            <span>
              (+48)&nbsp;538&nbsp;538&nbsp;757
            </span>
          </a>
          <img class="mr-2" src="../assets/images/mail.svg" alt="mail">
          <a class="mr-5" href="mailto://zawieziemy.pl@gmail.com">zawieziemy.pl@gmail.com</a>
          <img class="mr-2" src="../assets/images/msg.svg" alt="msg">
          <a class="mr-5" href="https://m.me/zawieziemypl">m.me/zawieziemypl</a>
        </div>
        <div class="right flex">
          <img class="mr-2" src="../assets/images/icon-fb.svg" alt="msg">
          <img class="mr-2" src="../assets/images/icon-tiktok.svg" alt="msg">
          <img class="mr-2" src="../assets/images/icon-instagram.svg" alt="msg">
        </div>
      </div>
    </div>
    <nav class="menu flex lg:max-w-[1024px] mx-auto flex justify-between items-center h-[96px]">
      <div class="logo flex-1">
         <img class="mr-2" src="../assets/images/logo-tex-S.svg" alt="logo">
      </div>
        <button type="button" class="inline-flex items-center p-2 justify-center md:hidden">
           <span class="sr-only">Open main menu</span>
           <img class="mr-2" src="../assets/images/navi.svg" alt="navi">
      </button>
      <div class="right hidden md:block">
        <a href="#home" :class="{'underline decoration-[#F8CE08]': page == 0}" @click.prevent="page = 0">Home</a>
        <a href="#about" :class="{'underline decoration-[#F8CE08]': page == 1}" @click.prevent="page = 1">O nas</a>
        <a href="#kontakt" :class="{'underline decoration-[#F8CE08]': page == 2}" @click.prevent="page = 2">Kontakt</a>
      </div>
    </nav>
    <!-- Home page start -->
    <div v-if="page == 0" class="lg:max-w-[1024px] mx-auto">
      <section id="hero" class="grid grid-cols-2 gap-4   grid-flow-col auto-cols-max">
        <div class="col-5">
          <div>
            ZawiezieMy... Ciebie, Twoje auto i Twoje rzeczy!
          </div>
          <div class="small mt-5">
            Naszym priorytetem jest Twoje bezpieczeństwo i komfort. Stawiamy na indywidualne podejście, dostosowując się do Twoich potrzeb.
          </div>
          <a class="btn btn-primary bg-yellow text-black" href="tel://0048538538757">
            <i class="phone"></i>
            Zadzwoń
          </a>
          <a href="btn btn-secondary" class="btn">Zapoznaj się z ofertą</a>
        </div>
        <div class="col-7">
          <div class="carousel  flex- gap-2 overflow-auto -- [&>*>img]:h-[400px] [&>*>img]:max-w-[unset] [&>div]:inline-block" style="white-space: nowrap;">
            <div class="slide">
              <img src="./hero-slide-taxi 2.png" alt="Taxi Bełchatów, car, roof">
            </div><div>
              <img src="./hero-slide-laweta.png" alt="Pomoc drogowa Bełchatów">
            </div><div>
              <img src="./hero-slide-bus.png" alt="Przewóz osób Bełchatów">
            </div>
          </div>
        </div>
      </section>
      <section id="oferta">
        <div class="title">
          <div class="text">Oferta</div>
          <span class="spacer">////</span>
        </div>
        <h2>Ty wyznaczasz cel, my znajdziemy najlepszą drogę.</h2>
        <div>
          <ul class="list-decimal hover:[&>*]:list-disc md:columns-2">
            <li>Usługi na terenie Bełchatowa i okolicy, w całej Polsce oraz zagranicą</li>
            <li>Gwarancja wygody i punktualności</li>
            <li>Dostępność 24/7</li>
            <li>Komfort i bezpieczeństwo</li>
            <li>Idealne na codzienne dojazdy, specjalne okazje i pilne potrzeby</li>
          </ul>
        </div>
      </section>
      <section id="features">
        <div class="row lg:flex">
          <div class="col">
            <h3>Usługi taxi</h3>
            <div class="img" contenteditable>
              <img src="./feat-1-taxi.png">
            </div>
            <div>
              <ul>
                <li>przewóz do 4 osób</li>
                <li>szybki czas realizacji</li>
                <li>nocne przewozy – bezpieczny powrót do domu po imrezach</li>
                <li>przejazdy do pracy i z pracy </li>
                <li>duży bagażnik </li>
                <li>przewozimy na terenie całej Polski (z i do Bełchatowa)</li>
              </ul>
            </div>
          </div>
          <!--  -->
          <div class="col">
            <h3>Przewóz osób busem</h3>
            <div class="img" contenteditable>
              <img src="./feat-2-transport.png">
            </div>
            <div>
              <ul>
                <li>przewóz do 8 osób</li>
                <li>przyjęcia okolicznościowe (wesela, komunie i inne imprezy rodzinne)</li>
                <li>wieczory kawalerskie i panieńskie, dyskoteki i inne</li>
                <li>transfery na lotniska i dworce</li>
                <li>cała Polska i zagranica</li>
              </ul>
            </div>
          </div>
          <!--  -->
          <div class="col">
            <h3>Pomoc drogowa</h3>
            <div class="img" contenteditable>
              <img src="./feat-3-service.png">
            </div>
            <div>
              <ul>
                <li>awaryjne odpalanie pojazdu</li>
                <li>dowóz paliwa</li>
                <li>pomoc na miejscu po awarii</li>
                <li>wymiana koła</li>
                <li>Bełchatów i okolice, trasy A1, A2, S8 i DK74</li>
              </ul>
            </div>
          </div>
          <!--  -->
          <div class="col">
            <h3>Autoholowanie</h3>
            <div class="img" contenteditable>
              <img src="./feat-4-hol.png">
            </div>
            <div>
              <ul>
                <li>pojazdy sprawne, uszkodzone i powypadkowe</li>
                <li>pomoc po kolizji drogowej</li>
                <li>pojazdy do 1,5 tony</li>
                <li>pojazdy osobowe, motocykle, małe maszyny rolnicze i inne</li>
                <li>przewóz do 2 osób</li>
                <li>na terenie całej Polski</li>
              </ul>
            </div>
          </div>
          <!--  -->
        </div>
      </section>
      <section id="opinie">
        <div class="title">
          <div class="text">Opinie</div>
          <span class="spacer">////</span>
        </div>
        <h2>Nie wierz nam na słowo, sprawdź co mówią o nas inni.</h2>
        <div>
          <ul class="carousel lg:flex">
            <li class="slide">
              <figure>
                <blockquote>
                  Polecam, profesjonalne podejście, szybka reakcja, samochód mimo ciężkich warunków wyciągnięty od razu.
                </blockquote>
                <figcaption>Marysia Ch.<br>
                  via. Facebook</figcaption>
              </figure>
            </li>
            <!--  -->
            <li class="slide">
              <figure>
                <blockquote>
                  Polecam! Człowiek godny zaufania i polecania. Bezproblemowo przyjechał po auto w środku nocy w weekend!
                </blockquote>
                <figcaption>Rafał<br>
                  via. Google</figcaption>
              </figure>
            </li>
            <!--  -->
            <li class="slide">
              <figure>
                <blockquote>
                  Profesjonalne usługi, przystępne i konkurencyjne ceny, sprawne i szybkie działanie 24/7. Polecam w 100%!
                </blockquote>
                <figcaption>Angelina S.<br>
                  via. Google</figcaption>
              </figure>
            </li>
          </ul>
        </div>
      </section>
      <section id="map" @click="map += 1, map %= 4">
        <div class="title">
          <div class="text">Mapa</div>
          <span class="spacer">////</span>
        </div>
        <!-- <button @click="map += 1, map %= 4">dalej</button> -->
        <div v-show="map % 4 == 0" contenteditable="false">
          <img src="./mapa-0.png">
        </div>
        <div v-show="map % 4 == 1" contenteditable="false">
          <img src="./mapa-1.png">
        </div>
        <div v-show="map % 4 == 2" contenteditable="false">
          <img src="./mapa-2.png">
        </div>
        <div v-show="map % 4 == 3" contenteditable="false">
          <img src="./mapa-3.png">
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
            Firma zawieziemy powstała w 2023 r. Jednak z transportem jesteśmy związani od kilku lat. Przez ten okres zdobyliśmy spore doświadczenie przede wszystkim na trasach międzynarodowych.
          </p>
          <p>
            Dzięki bogatemu doświadczeniu możemy świadczyć usługi na najwyższym poziomie, dbając o satysfakcję oraz bezpieczeństwo naszych klientów – zarówno tych obecnych, jak i nowych.
          </p>
          <p>
            Działamy głównie w Bełchatowie i okolicach, ale obsługujemy również zlecenia na terenie całego kraju oraz poza jego granicami.
          </p>
        </div>
        <div class="flex-1">
          <img src="./about-col-2nd.png" alt="">
        </div>
      </div>
    </div>
    <!-- About end -->
    <!-- Kontakt start -->
    <div v-show="page == 2">
      <div class="flex max-w-full">
        <div class="flex-1">
          <img src="./contact-col-1st.png" alt="">
        </div>
        <div class="flex-1">
          <img src="./contact-col-2nd.png" alt="">
        </div>
      </div>
    </div>
    <!-- Kontakt end -->
    <section id="footer" class="dark:bg-[#262523] dark:text-[#C7C7C4]">
      <div contenteditable="false">
        <img src="./footer-mock.png" alt="">
      </div>
      <hr>
      <div>
        <span>
          Copyright &copy; 2024
        </span>
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
  components: {
  },
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
    }
  },
  watch: {
    page(v) {
      location.hash = ['home', 'about', 'kontakt'][v]
    },
  },
})
</script>
