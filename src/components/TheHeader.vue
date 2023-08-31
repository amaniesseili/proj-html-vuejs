<script>
export default{
  props:{
    navigationItems:Array   // 2-VOCI MENU: ricevo l'array come propse lo uso per popolare le voci
  }

}

</script>

<template>
  <header>
    <div class="logo">
      <img src="" alt="">
    </div>

    <nav>
      <div class="navigation">
        <!-- 3-VOCI MENU: creo il ciclo for  -->
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
  
}


</style>