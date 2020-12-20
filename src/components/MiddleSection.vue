<template>
  <div class="all">
    <div class="title">
      <h1 id="page-title">A&E TOWS, LLC</h1>
    </div>
    <div class="container">
      <div class="img-container">
        <b-img class="img" :src="this.firstImage"></b-img>
        <b-img class="img" :src="this.secondImage"></b-img>
        <b-img class="img" :src="this.thirdImage"></b-img>
      </div>
      <div class="ul-container">
        <h3>WE GLADLY OFFER THE FOLLOWING SERVICES:</h3>
        <ul id="service-list">
          <li><font-awesome-icon :icon="myIcon" />Towing Services</li>
          <li><font-awesome-icon :icon="myIcon2" />Tire Changes</li>
          <li><font-awesome-icon :icon="myIcon3" />Wench Services</li>
          <li><font-awesome-icon :icon="myIcon4" />Jump Starts</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faCar, faTools, faCog, faCarBattery } from '@fortawesome/free-solid-svg-icons'
import image1 from '../assets/IMG_0497.jpeg'
import image2 from '../assets/IMG_0498.jpeg'
import image3 from '../assets/ae_towing_truck.jpg'
export default {
  // eslint-disable-next-line space-before-function-paren
  head() {
    return {
      script: [
        {
          src:
            'https://cdnjs.cloudflare.com/ajax/libs/jquery/3.1.1/jquery.min.js'
        }
      ],
      link: [
        {
          rel: 'stylesheet',
          href: 'https://fonts.googleapis.com/css?family=Roboto&display=swap'
        }
      ]
    }
  },
  // eslint-disable-next-line space-before-function-paren
  data() {
    return {
      firstImage: image1,
      secondImage: image2,
      thirdImage: image3,
      myIcon: faCar,
      myIcon2: faTools,
      myIcon3: faCog,
      myIcon4: faCarBattery
    }
  },
  components: { FontAwesomeIcon }

}
</script>

<style scoped>
.all {
  height: 105vh;
}
h3 {
  margin-top: 30px;
  color: yellow;
}
.container {
  margin-top: 5%;
}
* {
  font-family: Roboto, sans-serif;
  background-color: #000;
}
.title {
  text-align: center;
  color: yellow;
}
.all {
  height: 100%;
}
.container {
  width: 100%;
  display: flex;
  flex-direction: column;
  margin: 0 auto;
  align-content: center;
  place-items: center;
}
ul {
  margin: 0;
  padding: 0;
  min-width: 100vw;
  width: 100%;
  display: flex;
  justify-content: space-around;
  margin-top: 30px;
}
li {
  list-style-type: none;
  background-color: yellow;
  font-size: 22px;
  width: 350px;
  border: 1px solid white;
  border-radius: 25px;
  margin: 1%;
  padding: 3%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
svg {
  color: #000;
  background-color: yellow;
}
.img {
  width: 325px;
  height: 275px;
  border-radius: 25px;
  border: 1px solid #fff;
}

.img-container {
  display: flex;
  justify-content: space-between;
  width: 100%;
}
#page-title {
  padding-top: 1%;
}
@media (max-width: 1200px) {
  .all {
    height: 100%;
  }
  .img-container {
    place-items: center;
    flex-direction: column;
  }
  .img {
    margin: 3%;
    width: 475px;
    height: 375px;
  }
  .ul-container {
    margin: 0;
    padding: 0;
    min-width: 100vw;
    width: 100%;
    margin-bottom: 3%;
  }
}
</style>
