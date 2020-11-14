<template>
  <div id="app">
    <NavBar/>
    <router-view></router-view>
    <Footer/>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar'
import Footer from '@/components/Footer'

export default {
  name:"app",
    components:{
      NavBar,
      Footer
    }
  
}
</script>
