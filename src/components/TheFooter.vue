<script>
export default{
  props:{
    footerItems:Array,              //array voci menu footre
    contactInfo:Object             //ogetto contact info add.tel,email
  }

}

</script>

<template>
  <footer>
    <div class="container">
      <div class="row">
        <div class="col-3">
          <div class="footer-logo">
            <img src="src/assets/img/avada-food-logo-footer.png" alt="">
            <div class="social-icons">
              <i class="fa-brands fa-facebook-f"></i>
              <i class="fa-brands fa-instagram"></i>
              <i class="fa-brands fa-twitter"></i>
              <i class="fa-brands fa-youtube"></i>
            </div>
          </div>
        </div>
        <!-- footer, seconda colonna voci di menu  -->
        <div class="col-3">
          <div class="footer-menu h-100">
            <ul>
              <li class="footer-menu-li" v-for="item in footerItems" :key="item">{{item}}</li>
            </ul>
          </div>
        </div>
        <!-- footer, terzza colonna voci di menu  -->
        <div class="col-3">
          <div class="footer-contact h-100">
            <h6>CONTACT</h6>
            <P>{{contactInfo.address}}</P>
            <p>{{contactInfo.phoneNumber}}</p>
            <p>{{contactInfo.email}}</p>
          </div>
        </div>
        <!-- footer, terzza colonna voci di menu  -->
        <div class="col-3">
          <div class="footer-app">
            <h6>GET OUR APP</h6>
            <img class="" src="src/assets/img/download-android.png" alt="" style="width:;">
            <img src="src/assets/img/download-app-store-200x66.png" alt="">
          </div>
        </div>
      </div>
    </div>
    <div class="footer-copyright">
      <small>copyright 2012-2020 - Avada ThemeFusion - All Rights Reserved - Powered by WordPress</small>

    </div>
  </footer>

</template>

<style lang="scss" scoped>
@use "../scss/partials/variables" as *;

.fa-brands{
  padding-left: 1rem;
  color: gray;
  margin-top: 7rem;
}
h6{
  margin-bottom: 2rem;
  color: $primary-color;
}
.footer-menu{
  border-left: 1px dashed grey;
  padding-left: 2rem;

}
.footer-contact{
  border-left: 1px dashed grey;
  padding-left: 2rem;
  color: grey;
  
  p{
    margin-bottom: 2rem;
  }

}

.footer-app{
  border-left: 1px dashed grey;
  padding-left: 2rem;
}
.footer-app img{
  width: 90%;
  margin-bottom: 1rem;
}

.footer-copyright{
  height: 80px;
  background-color: $secondary-color;
  text-align: center;
  vertical-align: middle;
  padding-top: 2rem;
  margin-top: 2rem;
}
.footer-menu-li{
  list-style: none;
  margin-bottom: 1.5rem;
  font-weight: bold;
}


</style>