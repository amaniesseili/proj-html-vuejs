<script>
export default{
  props:{
    navigationItems:Array   // 2-VOCI MENU: ricevo l'array come propse lo uso per popolare le voci
  }

}

</script>

<template>
  <header>

    <div class="container">
      <div class="header-info">
        <div class="d-flex">
          <p><small>Download App</small></p>
          <p class="ms-5"><small>Advertise with us</small></p>
        </div>
        <div class="social-icons">
          <i class="fa-brands fa-facebook-f"></i>
          <i class="fa-brands fa-instagram"></i>
          <i class="fa-brands fa-twitter"></i>
          <i class="fa-brands fa-youtube"></i>
        </div>
      </div>
    </div>



    <div class="logo">
      <img class="logo-img" src="../assets/img/avada-food-logo-2x.png" alt="avad-food-logo">
    </div>

    <!-- 3-VOCI MENU: creo il ciclo for  -->
    <nav>
      <div class="navigation">
        <div class="nav-menu" v-for="item in navigationItems" :key="item.id">
          {{item.title}}
        </div>
      </div>
    </nav>



  </header>



</template>

<style lang="scss" scoped>
@use "../scss/partials/variables" as *;



.navigation{
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 4rem;
  margin-bottom: 1rem;
  padding-bottom: 2rem;
  margin-bottom: 2rem;

}
.nav-menu{
  padding-bottom:0.5rem;
}
.nav-menu:hover {
  color: $primary-color;
  border-bottom: 2px solid $primary-color;
}


.logo{
  display:flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 2rem;
  margin-top: 2rem;

}

.logo-img{
  width: 150px;
}

.header-info{
  display: flex;
  justify-content: space-between;
}



</style>