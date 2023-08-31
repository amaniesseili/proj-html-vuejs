<script >
import TheHeader from './components/TheHeader.vue';
import TheMain from './components/TheMain.vue';
import TheFooter from './components/TheFooter.vue';



export default {
    components: {  
      TheFooter,
      TheHeader,
      TheMain
    },
    data() {
      return {
        navigationListItem:[       // 1- VOCI MENU: creo un array per popolare le voci->props->template<TheHeader:nav.. >
          { id: 1, title: "Home" },
          { id: 1, title: "Recipes" },
          { id: 1, title: "Places" },
          { id: 1, title: "Blog" },
          { id: 1, title: "About" },
          { id: 1, title: "Contact" }
        ]
      }
    },
}
</script>

<template>
  <TheHeader :navigationItems="navigationListItem"></TheHeader> 

  <TheMain></TheMain>

  <TheFooter></TheFooter>
  
</template>

<style lang="scss">

</style>
