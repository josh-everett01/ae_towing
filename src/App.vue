/* eslint-disable space-before-function-paren */
<template>
  <div id="app">
    <h4>For emergency service please call 972-329-1234</h4>
    <div class="main-img" :style="{ backgroundImage: `url(${image})` }">
      <div class="h1-div">
        <h1>A&E TOWS, LLC</h1>
        <h3>103 Gross rd. Ste # D-24</h3>
        <h3>Mesquite, TX 75149</h3>
        <div class="button-div">
          <b-button v-on:click="this.goToServices">SERVICES</b-button>
          <b-button v-on:click="this.goToContact">CONTACT</b-button>
        </div>
      </div>
    </div>
    <div class="middle">
      <MiddleSection />
    </div>
    <div class="contact">
      <Contact />
    </div>
  </div>
</template>

<script>
import carImg from './assets/pexels-mike-943930.jpg'
import MiddleSection from './components/MiddleSection.vue'
import Contact from './components/Contact'

export default {
  name: 'App',
  // eslint-disable-next-line space-before-function-paren
  data() {
    return {
      image: carImg
    }
  },
  methods: {
    goToServices: function () {
      window.scrollTo(0, 715)
    },
    goToContact: function () {
      window.scrollTo(0, 1390)
    }
  },
  components: { MiddleSection, Contact }
}
</script>

<style>
body {
  margin: 0;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  display: flex;
  flex-direction: column;
}
button {
  padding: 10px;
  margin-top: 10px;
  margin-right: 2%;
  margin-left: 2%;
}
* {
  font-family: Roboto, sans-serif;
}
h4 {
  margin: 0;
  background: #000;
  text-transform: uppercase;
  text-align: center;
  color: yellow;
}
.main-img {
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  place-items: center;
  width: 100%;
  min-height: 100vh;
  max-height: 100vh;
  background-size: cover;
  background-repeat: no-repeat;
}
.h1-div {
  background: rgba(0, 0, 0, 0.6);
  font-family: Arial, Helvetica, sans-serif;
  padding-top: 40px;
  padding-bottom: 20px;
  width: 100%;
  text-align: center;
  color: yellow;
  display: flex;
  flex-direction: column;
}

h1 {
  font-size: 72px;
}
</style>
