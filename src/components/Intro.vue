<script>
export default{
  data(){
    return{
      showIntro: true,
      indexSlide: false,
      analisiSlide: false,
      structureSlide: false,
    };
  },
  mounted(){
    setTimeout(() => {
        this.showIntro = false;      // 1- nascondo la prima slide dopo 5s 
        this.indexSlide = true;    // 2- mostro la seconda slide 
    }, 2500);

    setTimeout(()=>{
      this.indexSlide= false;     //3- nascondo la seconda slide dopo altre 10s
      this.analisiSlide= true;    // 4- mostro la terzza slide 
    }, 5000);

    setTimeout(()=>{
      this.analisiSlide= false;     //5- nascondo la terza slide dopo altre 90s
      this.structureSlide= true;     //6-mostro la quarta slide 
    }, 90000);

    setTimeout(()=>{
      this.structureSlide= false      //7- structureSlide si scompare dopo 100s
    }, 100000);
  },

};
</script>

<template>

    <!-- slide-1 intro -->
    <div v-if="showIntro" class="intro">

      <div class="header"></div>

      <section class="cards">
        <div class="container ">
          <div class="card-container d-flex justify-content-between h-100  ">
            <div class="card me-5" style="width: 20rem;">
                <img src="src/assets/img/floria.jpg" class="card-img-top" alt="...">
              <div class="card-body ">
                <h5 class="text-center">MAESTRO: <br> Leica Florian Robert</h5>
              </div>
            </div>
            
            <div class="card me-5" style="width: 20rem;">
              <img src="src/assets/img/ama.jpg" class="card-img-top" alt="...">
              <div class="card-body ">
                <h5 class="text-center">STUDENTE: <br> Amani Esseili</h5>
              </div>
            </div>

          <div class="card " style="width: 20rem;">
              <img src="src/assets/img/boolean-logo.png" class="card-img-top" alt="...">
            <div class="card-body ">
              <h5 class="text-center">TUTOR: <br> Alessio Crea & Michele Spiller</h5>
            </div>
        </div>
          </div>
        </div>

        <h1>FOOD AVADA : WordPress Theme!</h1>
      </section> 
    </div>

<!-- slide 2- index  -->
<div v-if="indexSlide" class="slid">

  <div class="header"></div>

  <div class="index  d-flex">
    <div>
      <i class="fa-solid fa-magnifying-glass-chart"></i>
      <h3 class="text-center mt-5 ms-5 ps-1">Analisi Layout</h3>
    </div>
    <div>
      <i class="fa-solid fa-folder-tree"></i>
      <h3 class="text-center mt-5 ms-5 ps-4">Struttura</h3>
    </div>
    <div>
      <i class="fa-solid fa-code"></i>
      <h3 class="text-center mt-5 ms-5 ps-4">Codice</h3>
    </div>
  </div>

</div>

<!-- slide 3- Analisi layout  --> 
<div v-if="analisiSlide" class="analisi-layout">
  <div class="container d-flex">
    <div class="row">
      <div class="col-6 h-100">
        <img src="src/assets/img/ANALYSIS LAYOUT.jpg" class="analisi-img" alt="">
      </div>
    </div>

    <div class="col-6 analisi-">
      <h3>Struttura del Layout</h3>
      <p>Il layout del sito è suddiviso in tre sezioni princhipali: <b>Header</b><b> Main</b> e <b>Footer</b>.</p>
      
      <div class="header-analysis">
        <h4>Header</h4>
        <ul>
          <li> La sua struttura e semplice presenta il <b>Logo</b> e il <b>Menu di Navigazione</b></li>
        </ul>
      </div>
      <div class="main-analysis">
        <h4>Main</h4>
        <p>Il Main contiene <b> 6 sezioni</b> ognuna con un contenuto ben definito e layout molto simile </p>
        <ul>
          <li><b> Containers di Bootstrap</b></li>
          <p>i container sono <b> uguali</b> in tutti le sezioni, con <b>spaziatura specifica</b> sia sopra che sotto il containerper garantire una layout equilibrato. </p>
        </ul>
        <ul>
          <li><b>Contenuto Centrato </b></li>
          <p>Tanti sezioni hanno il <b>Test Centrato </b>.</p>
        </ul>
        <ul>
          <li><b>Card Bootstrap</b></li>
          <p>Le Card di Bootstrap sono <b>identici</b> in ogni sezione, ognuna con immagine e corpo informativo.</p>
        </ul>
        <ul>
          <li><b>overlay sull'immagine</b></li>
          <p>Quasi tutti gli immagine hanno un overlay con un test centralizato.</p>
        </ul>
        <ul>
          <li><b>Scelta dei Colori</b></li>
          <p>I colori utilisati riflettono la tema culinario del sito e trasmettono specifici significati:
            <ul>
              <li><b>Sfondo Pulito e Neutro</b></li>
              <p>il colore dello sfondo e chiaro e neutro per creare un ambiente <b>Accogliente</b> e <b>Pulito</b> . </p>
            </ul>
            <ul>
              <li><b>Colore Arancione</b></li>
              <p>L'uso del colore arancione rapresenta energia e movimento, trasmetendo una senzazione di accoglienza e creativitàai visitatori. </p>
            </ul>
          </p>
        </ul>
      </div>
    </div>
  </div>
</div>
<!-- slide 4- structure   --> 
<div v-if="structureSlide" class="structure">
  <div class="content-container">
    <div class="row">
      <div class="col-5">
        <div class="titolo-slide">
          <h2>La Struttura</h2>
          <p></p>
        </div>
      </div>
      
      <div class="col-5">
        <div class="structure-img">
          <img src="src/assets/img/STRUCTURE.jpg" alt="">
        </div>
      </div>
    </div>
  


  </div>


</div>



</template>

<style lang="scss" scoped>
@use "../scss/partials/variables" as *;


.header{
  min-height: 400px;
  background-image: url(../assets/img/1-jumbo.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  opacity: 0.5;
  width: 100%;
  border-left: 70px solid orangered;
  border-top: 70px solid orangered ;
  margin-bottom: 500px;

}

.cards{
  position: absolute;
  top: 350px;
  left: 50%;
  transform: translatex(-50%);
  
}

h1{
  margin-top: 30px;
  font-size: 30px;
  font-weight: bold;
  text-align: center;
  vertical-align: middle;
  color: black;
  margin-bottom: 50px;
}

.fa-solid{
  background-color: $primary-color;
  padding: 2rem;
  font-size: 70px;
  color: white;
  margin-left: 5rem;
  border-radius: 50%;
  aspect-ratio: 1/1;
  border: 2px solid white;
  width: 200px;
  height: 200px;
  text-align: center;
  vertical-align: middle;
  padding-top: 4rem;
}
.index{

  position: absolute;
  top: 350px;
  left: 50%;
  transform: translatex(-50%);
}

.analisi-img{
  width: 160%;
  margin: 1rem;

}
.analisi-layout{
  border-top:3rem solid rgb(253, 118, 68) ;
  border-left:3rem solid rgb(253, 118, 68) ;
  padding-top: 1rem;
}

</style>