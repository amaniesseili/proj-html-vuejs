<script>
export default{

}

</script>

<template>
  <main>
    <section class="jumbo">
      <div class="jumbo-img"></div>

      <div class="jumbo-content">
        <div class="row">
          <div class="col-5"></div>
          <div class="col-2">
            <button class="jumbo-btn">TODAY'S PICK</button>
          </div>
        </div>
        <div class="row">
          <div class="col-5"></div>
          <div class="col-3">
            <div class="jumbo-text text-center bg-light pt-5 pb-4 rounded-3">
              <h2>Food Corner: Top Japanese <br>Resaurant for Sushi</h2>
              <small>March 25.2019</small>
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
}
.jumbo-btn{
  background-color: $primary-color;
  color: white;
  border-radius: 10px;
  padding: 0.2rem 1rem;
}

</style>