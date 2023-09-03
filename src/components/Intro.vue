<script>
export default{
  data(){
    return{
      showIntro: true,
      indexSlide: false,
      analisiSlide: false,
    };
  },
  mounted(){
    setTimeout(() => {
        this.showIntro = false;      // 1- nascondo la prima slide dopo 5s 
        this.indexSlide = true;    // 2- mostro la seconda slide 
    }, 5000);

    setTimeout(()=>{
      this.indexSlide= false;     //3- nascondo la seconda slide dopo altre 10s
      this.analisiSlide= true;
    }, 10000);

    setTimeout(()=>{
      this.analisiSlide= false;     //3- nascondo la terza slide dopo altre 45s
    }, 40000);
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

<!-- slide 2- Analisi layout  -->
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

<!-- slide 2- Analisi layout  --> 
<div v-if="analisiSlide" class="analisi-layout">
    <p>analisi layout  </p> 
</div>



</template>

<style lang="scss" scoped>
@use "../scss/partials/variables" as *;

p{
  font-size: 10px;
}
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

</style>