<script>
export default{
  data(){
    return{
      showIntro: true,
    };
  },
  mounted(){
    setTimeout(() => {
        this.showIntro = false; //per nascondere il componente del intro dopo 10s
    }, 10000);
  },

};
</script>

<template>
  <div>
    <div v-if="showIntro" class="intro">

      <p>benvenuti al mio progetto </p>
    </div>
  </div>

</template>

<style lang="scss" scoped>
@use "../scss/partials/variables" as *;

.intro{
  width: 100%;
  height: 100wh;
}

p{
  font-size: 100px;
}
</style>