<template>
  <header>
    <div class="box-logo">
      <!-- <i class="fa-brands fa-spotify"></i> -->
    </div>
    <div class="bottone-sel">
      <button type="button" class="btn btn-light">Seleziona</button>
    </div>

  </header>
</template>

<script>
export default {
name: "HeaderComponent",
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';
@import '../assets/style/general';

header{
  height: 60px;
  background-color: $primary-color;
  padding: 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  .box-logo{
    width: 40px;
  }
}

</style>