<template>
  <main>
    <div class="container">
      
    <CardCd v-for="(item,index) in CdArray" :key="index" :CdItem="item"/>
      
    </div>
  </main>
</template>

<script>
import axios from 'axios';
import CardCd from './CardCd.vue';

export default {
    name: "MainComponent",
    data() {
        return {
            baseURL: "https://flynn.boolean.careers/exercises/api/array/music",
            CdArray: [],
        };
    },
    mounted() {
        this.getAPI();
    },
    methods: {
      getAPI(){
      axios.get(this.baseURL)
      .then(result => {
      this.CdArray = result.data.response;
      console.log(this.CdArray);
    })
  }
    },
    components: { CardCd }
}
</script>

<style lang="scss" scoped>

main{
  background-color:rgb(30, 45, 59);
  .container{
    display:flex;
    flex-wrap: wrap;
    padding:20px

  }

 
}


</style>