<script>
export default{
  data(){
    return{
      showIntro: true,
      analisiSlide: false,
    };
  },
  mounted(){
    setTimeout(() => {
        this.showIntro = false;      // 1- nascondo la prima slide dopo 10s 
        this.analisiSlide = true;    // 2- mostro la seconda slide 
    }, 10000);

    setTimeout(()=>{
      this.analisiSlide = false;     //3- nascondo la seconda slide dopo altre 10s
    }, 20000);
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
<div v-if="analisiSlide" class="slid">

  <p>questa e la seconda slide </p>

</div>




</template>

<style lang="scss" scoped>
@use "../scss/partials/variables" as *;


p{
  font-size: 200px;
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

</style>