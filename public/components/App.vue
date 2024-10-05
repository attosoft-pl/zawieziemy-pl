<template>
  <div class="mx-auto lg:max-w-[1024px] [&>*]:my-[20px] [&>*]:border [&>*]:border-black">
    <div class="header bg-[#F8CE08] text-black flex justify-between">
      <div class="left">
        <a href="tel://0048538538757">
          <i class="phone"></i>
          <span>
            +48&nbsp;538&nbsp;538&nbsp;757
          </span>
        </a>
        <a href="mailto://zawieziemy.pl@gmail.com">zawieziemy.pl@gmail.com</a>
        <a href="https://m.me/zawieziemypl">m.me/zawieziemypl</a>
      </div>
      <div class="right">
        [f]
        [t]
        [ig]
      </div>
    </div>
    <nav class="menu">
      <div class="logo">[logo]</div>
      <div class="right">
        <a href="#home">Home</a>
        <a href="#about">O nas</a>
        <a href="#kontakt">Kontakt</a>
      </div>
    </nav>
    <!-- Home page start -->
    <div>
      <section id="hero">
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
          <div class="carousel">
            <div class="slide">
              <img src="./carousel-taxi-1.webp" alt="Taxi Bełchatów, car, roof">
            </div>
            <div>
              <img src="./carousel-pomoc-drogowa.webp" alt="Pomoc drogowa Bełchatów">
            </div>
            <div>
              <img src="./carousel-przewoz-osob.webp" alt="Przewóz osób Bełchatów">
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
          <ul class="list-decimal hover:[&>*]:list-disc columns-2">
            <li>Usługi na terenie Bełchatowa i okolicy, w całej Polsce oraz zagranicą</li>
            <li>Gwarancja wygody i punktualności</li>
            <li>Dostępność 24/7</li>
            <li>Komfort i bezpieczeństwo</li>
            <li>Idealne na codzienne dojazdy, specjalne okazje i pilne potrzeby</li>
          </ul>
        </div>
      </section>
      <section id="features">
        <div class="row flex">
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
          <ul class="carousel flex">
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
      <section id="opinie">
        <div class="title">
          <div class="text">Mapa</div>
          <span class="spacer">////</span>
        </div>
        <div contenteditable="false">
          <img src="./mapa.png">
        </div>
      </section>
    </div>
    <!-- Home page end -->
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
    }
  }
})
</script>
