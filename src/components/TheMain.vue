<script>
export default{

}

</script>

<template>
  <main>
    <section class="jumbo">
      <div class="jumbo-img"></div>
      <div class="jumbo-content">
        <button class="jumbo-btn">TODAY'S PICK</button>
        
        <div class="jumbo-text text-center bg-light pt-4 pb-3">
          <h2>Food Corner: Top Japanese <br>Resaurant for Sushi</h2>
          <small>March 25.2019</small>
        </div>
      </div>
    </section>

    <section class="foodie-journal">
      <div class="container">
        <h5 class="text-center">FOODIE JOURNAL</h5>
        <div class="card-container d-flex">

          <div class="card" style="width: 18rem;">
            <img src="../assets/img/" class="card-img-top" alt="...">
            <div class="card-body">
              <h5>Food Corner: Top Japanese <br> Restaurant for Sushi</h5>
              <small>By admin - March 25th.2019</small>

            </div>
          </div>

          <div class="card" style="width: 18rem;">
            <img src="..." class="card-img-top" alt="...">
            <div class="card-body">
              <h5>Roundup: My New Favourite <br>Recipes For Healthy Living</h5>
              <small>By admin - March 25th.2019</small>
            </div>
          </div>

          <div class="card" style="width: 18rem;">
            <img src="..." class="card-img-top" alt="...">
            <div class="card-body">
              <h5>Why These Toasts With Tea are<br>My New Favorite</h5>
              <small>By admin - March 25th.2019</small>
            </div>
          </div>
        </div>

      </div>




    </section>

  </main>


</template>

<style lang="scss" scoped>
@use "../scss/partials/variables" as *;

.jumbo{
  min-height: 600px;
  background-image: url(../assets/img/1-jumbo.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  width: 100%;
  position: relative;
}
.jumbo-btn{
  background-color: $primary-color;
  color: white;
  border-radius: 10px;
  padding: 0.2rem 1rem;
}
.jumbo-content{
  position: absolute;
  top:50%;
  left: 50%;
  transform: translate(-50%, -50%);
  padding: 3rem;
  border-radius: 5px; 
}
.jumbo-btn{
  position: absolute;
  top: 30px;
  left: 50%;
  transform: translatex(-50%);
  cursor: pointer;
}

</style>