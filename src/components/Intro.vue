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
    }, 3000);

    setTimeout(()=>{
      this.indexSlide= false;     //3- nascondo la seconda slide dopo altre 10s
      this.analisiSlide= true;    // 4- mostro la terzza slide 
    }, 10000);

    setTimeout(()=>{
      this.analisiSlide= false;     //5- nascondo la terza slide dopo altre 90s
      this.structureSlide= true;     //6-mostro la quarta slide 
    }, 100000);

    setTimeout(()=>{
      this.structureSlide= false      //7- structureSlide si scompare dopo 100s
    }, 160000);
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
<div v-if="indexSlide" class="slide">

  <div class="header-slide2"></div>

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
  <div class="container mb-5">
    <h1>Progetto</h1>

    <P>Replicare il layout proposto solo in versione <b>DESKTOP</b> usando HTML,CSS/SCSS, Vue.js e Vite. Organizzare il progetto i almeno tre componente <b>Header</b> <b>Main</b> <b>Footer</b> e popolare dinamicamente le voci di menu nell'Header e Footer con Vue.js </P>

  </div>



</div>

<!-- slide 3- Analisi layout  --> 
<div v-if="analisiSlide" class="slide-layout">
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
        <div class="row">
          <h4>Header & Footer</h4>
          <div class="col-11 p-color">
            <ul>
              <li>Struttura e semplice presenta il <b>Logo</b> e il <b>Menu di Navigazione</b> e<b> contatto</b> </li>
            </ul>
          </div>
        </div>


      <div class="main-analysis">
        <div class="row">
          <h4>Main</h4>
          <p>Il Main contiene <b> 6 sezioni</b> ognuna con un contenuto ben definito e layout molto simile </p>

          <div class="col-5 container-bootstrap">
            <ul>
              <li><b> Containers di Bootstrap</b></li>
              <p>i container sono <b> uguali</b> in tutti le sezioni, con <b>spaziatura specifica</b> sia sopra che sotto il containerper garantire una layout equilibrato. </p>
            </ul>
          </div>
          <div class="col-5 Contenuto-Centrato">
            <ul>
              <li ><b>Contenuto Centrato </b></li>
              <p>Tanti sezioni hanno il <b>Test Centrato </b>.</p>
            </ul>
          </div>

        </div>
        <div class="row">
          <div class="col-5 Card-Bootstrap">
            <ul>
              <li><b>Card Bootstrap</b></li>
              <p>Le Card di Bootstrap sono <b>identici</b> in ogni sezione, ognuna con immagine e corpo informativo.</p>
            </ul>
          </div>
          <div class="col-5 overlay-analysis">
            <ul>
              <li><b>overlay sull'immagine</b></li>
              <p>Quasi tutti gli immagine hanno un overlay con un test centralizato.</p>
            </ul>
          </div>
        </div>
        <div class="row">
          <h5>Scelta dei Colori</h5>
          <p>I colori utilisati riflettono la tema culinario del sito e trasmettono specifici significati:</p>
          <div class="col-5 me-4  p-color">
            <ul>
              <li><b>Sfondo Pulito e Neutro</b></li>
              <p>il colore dello sfondo e chiaro e neutro per creare un ambiente <b>Accogliente</b> e <b>Pulito</b> . </p>
            </ul>
          </div>
          <div class="col-5 ms-4 p-color">
            <ul>
              <li><b>Colore Arancione</b></li>
              <p>l'arancione rapresenta l'energia, trasmetendo una senzazione di accoglienza ai visitatori. </p>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</div>




<!-- slide 4- structure   --> 
<div v-if="structureSlide" class="structure ">
  <div class="content-container slide-layout">
    <div class="container">

      
      <div class="row">
        <div class="col-6" >
          <div class="titolo-slide">
            <h2>Struttura del Progetto Vue.js</h2>
            <p class="fs-5 mt-4">Analisi dell'architettura del progetto Vue.js </p>
          </div>
          <h4 class="mb-4 mt-5 pt-5">Cartelle Principali</h4>

          <div class="row centered-text ms-3">
            <div class="col-2 bg-col ">
              <h4 >Assets</h4>
              <p>Immagine e Risorse</p>
            </div>
            <div class="col-2 bg-col">
              <h4>Partials</h4>
              <p>Varialbili Sass e mixins</p>
            </div>
            <div class="col-2 bg-col">
              <h4>Scss</h4>
              <p>File di stile</p>
            </div>
            <div class="col-2 bg-col">
              <h4>General</h4>
              <p>Dipendenze del progetto</p>
            </div>
          </div>

          <div>
            <h4 class="mb-4 mt-5 pt-5">Struttura dei componenti </h4>
          </div>

          <div class="row centered-text ms-3">
            <div class="col-3 bg-col theheader">
              <h4>TheHeader</h4>
              <p>E la parte superiore del sito.Contiene Logo e voci di menudi navigazione</p>
            </div>
            <div class="col-3 bg-col themain">
              <h4>TheMain</h4>
              <p>E il componente centrale, e rapresenta il contenuto del sito </p>
            </div>
            <div class="col-3 bg-col thefooter">
              <h4>TheFooter</h4>
              <p>Il piede della pagina. Contiene informazioni di contatto, e link utili piu il logo del marchio con il copyright</p>
            </div>
          </div>

        </div>
        
      <div class="col-5">
        <div >
          <img src="src/assets/img/STRUCTURE.jpg" class="structure-img" alt="">
      </div>
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
.header-slide2{
    min-height: 400px;
    background-image: url(../assets/img/1-jumbo.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    opacity: 0.5;
    width: 100%;
    border-left: 70px solid orangered;
    border-top: 70px solid orangered ;
    margin-bottom: 300px;

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
.slide-layout{
  border-top:3rem solid rgb(253, 118, 68) ;
  border-left:3rem solid rgb(253, 118, 68) ;
  padding-top: 1rem;
}

.structure-img{
  width: 95%;
  margin: 1rem;

}
.content-container{
  padding: 1rem ;
}

.centered-text{
  text-align: center;

}
.bg-col{
  background-color: $primary-color;color: white;
  padding: .2rem;
  margin-right:3rem ;
}
.theheader{
  background-color: #78DC94;
  
}
.themain{
  background-color: #D3ABE7;
}
.thefooter{
  background-color: #8ECECD;
  
}

.container-bootstrap{
  border: 5px solid #3379B4;
  margin-right: 3rem;
  margin-bottom: 1rem;
  margin-left: 2rem;
  padding: 0.2rem;
}
.Contenuto-Centrato{
  background-color: #87E5C0; 
  margin-bottom: 1rem;
  padding: 0.2rem;

}
.Card-Bootstrap{
  background-color: #DAAFF7;
  margin-right: 3rem;
  margin-bottom: 1rem;
  margin-left: 2rem;
  padding: 0.2rem;
}
.overlay-analysis{
  background-color: #FA779F;
  margin-right: 1rem;
  margin-bottom: 1rem;
  padding: 0.3rem;
}
.p-color{
  background-color: $primary-color;
  margin-left: 2rem;

}

</style>