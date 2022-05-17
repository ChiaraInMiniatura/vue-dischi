<template>
  <div class="cd-card">

    <div class="img-container">
      <img :src="CdItem.poster" alt="poster">
    </div>

    <div class="text-center">
      <h4>{{CdItem.title}}</h4>
      <span>{{CdItem.author}}</span><br>
      <span>{{CdItem.year}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardCd",
  props:{
    CdItem : Object,
  }

}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';
@import '../assets/style/general';

.cd-card{
  background-color: $primary-color;
  padding: 10px;
  width: calc((100% / 5) - 20px);
  padding-bottom: 40px;
  margin:0px 10px;
  margin-bottom: 20px;
  h4{
    text-transform: uppercase;
    color: white;
    font-size: 15px;
    margin-top: 10px;
  }
  span{
    color: grey;
  }
}  

</style>