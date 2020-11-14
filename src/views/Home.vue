<template>
  <div class="container-fluid text-white p-5 mb-0" style="background:#1B2838;">

    <div class="container menu" style="background:#366C90; padding:0px; display:inline-flex;list-style:none;">
        <b-nav-item-dropdown left >
          <template #button-content>
            <em style="{color:#D1DDE5;}:hover{color:black;}:active{color:black;}" >A tua loja</em>
          </template>
          <b-dropdown-item href="#" style="color:black">Profile</b-dropdown-item>
          <b-dropdown-item href="#" style="color:black">Sign Out</b-dropdown-item>
        </b-nav-item-dropdown>
        <b-nav-item-dropdown left >
          <template #button-content>
            <em style="{color:#D1DDE5;}:hover{color:black;}:active{color:black;}">Procurar</em>
          </template>
          <b-dropdown-item href="#">Profile</b-dropdown-item>
          <b-dropdown-item href="#">Sign Out</b-dropdown-item>
        </b-nav-item-dropdown>
        <b-navbar-nav class="mx-1">
          <b-nav-item href="#" class="px-3" >Loja de Pontos</b-nav-item>
        </b-navbar-nav>
        <b-navbar-nav class="mx-1">
          <b-nav-item href="#" class="px-3">Notícias</b-nav-item>
        </b-navbar-nav>
        <b-navbar-nav class="mx-1">
          <b-nav-item href="#" class="px-3">Laboratório Steam</b-nav-item>
        </b-navbar-nav>
        <b-nav-form class="ml-auto">
          <b-form-input size="sm" class="mr-sm-2" placeholder="Procurar na loja" 
          style="background:#316282;color:#D1DDE5;">
          </b-form-input>
          <b-button size="sm" class="my-2 my-sm-0" type="submit" style="background:#64B4E3;color:#304765;">
            <b-icon icon="search"></b-icon>
          </b-button>
        </b-nav-form>
    </div>

    <h1>Jogos no Steam</h1>
    <p style="color:#819997;">Encontra os jogos para PC mais recentes, mais vendidos e em promoção no Steam</p>
    <div >
    <img >
    </div>

     <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
      
    >
        <b-carousel-slide v-for="game in games.slice(0, 10)" :key="game.gameID">
        <template #img>
          <img
            class="d-block img-fluid w-100"
            width="1024"
            height="480"
            :src="game.thumb" :alt="game.title"
          >
        </template>
      </b-carousel-slide>
    </b-carousel>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'Home',
  data(){
    return{
      games:[]
    }
  },
  mounted() {
    axios.get('/deals?storeID=1&upperPrice=15').then(response => {
      this.games = response.data;
    })
  },
}

</script>

<style>
  html, body {
margin: 0;
padding: 0;
height: 100%;
}
footer{
bottom: 0;
position:absolute;
}
.nav-item:hover{
  background:#D1DDE5;
  color:black;
}
.nav-item a{
  color:#D1DDE5;
}
.nav-item a:hover{
  color:black;
}
</style>
