<template>
  <div class="wrapper-container">
    <NavBar></NavBar>
    <div class="content">
      <div class="loader" id="loader">
        <div class="wrapper">
          <span>Loading fonts</span>
          <div class="line"></div>
          <div class="subline inc"></div>
          <div class="subline dec"></div>
        </div>
      </div>
      <div class="part">
        <h2 :style="$store.state.primary">Hacktoberfest</h2>
        <p :style="$store.state.secondary">
          Hacktoberfest is a month-long celebration of open source software run by DigitalOcean in partnership with GitHub and Twilio. Hacktoberfest is open to everyone in our global community! Five quality pull requests must be submitted to public GitHub repositories.
        </p>
        <div class="author">
          <span v-show="$store.state.name != undefined" :style="$store.state.secondary">Fonts picked by</span>
          <a :href="$store.state.git" :style="$store.state.secondary" class="git">{{$store.state.name}}</a>
        </div>
      </div>
      <div class="part">
        <a href="https://hacktoberfest.digitalocean.com/">
          <img src="@/assets/hacktober.svg" alt="">
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from '../components/NavBar'

export default {
  name: 'Wrapper',
  components: {
    NavBar
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  mounted(){
    let url = 'https://github.com/itsvvishnu.png'
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
