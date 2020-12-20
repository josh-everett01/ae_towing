<template>
  <div id="main">
    <h1>CONTACT US</h1>
    <div class="form-map-div">
      <form action="https://formspree.io/xdowrapj" method="POST">
        <label>
          Your name:
          <input type="name" name="name" /> </label
        ><br />
        <label>
          Your email:
          <input type="text" name="_replyto" />
        </label>
        <label>
          Your message:
          <textarea
            name="message"
            placeholder="Please include a phone number if you wish to be contacted by phone"
          ></textarea>
        </label>

        <!-- your other form fields go here -->

        <button type="submit">Send</button>
      </form>
      <div class="map">
        <GmapMap
          class="gmap"
          :center="{ lat: 32.76999, lng: -96.61437 }"
          :zoom="10"
          map-type-id="terrain"
          style="width: 500px; height: 300px"
        >
          <GmapMarker
            :key="index"
            v-for="(m, index) in markers"
            :position="m.position"
            :clickable="true"
            :draggable="true"
            @click="center = m.position"
          />
        </GmapMap>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line space-before-function-paren
  data() {
    return {
      markers: [
        {
          position: {
            lat: 32.76999, lng: -96.61437
          },
          infoText: 'A&E Tows LLC'
        }
      ]
    }
  }
}
</script>

<style scoped>
#main {
  height: 100vh;
}
.gmap {
  border-radius: 25px;
}
.form-map-div {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}
form {
  font-size: 18px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 3%;
  width: 300px;
}

form button {
  width: 75px;
  border-radius: 25px;
}
form input {
  margin-top: 2%;
}

form label {
  margin: 0;
  padding: 0;
}

textarea {
  width: 300px;
}
.map {
  margin-bottom: 1%;
}
* {
  margin: 0;
  padding: 0;
  place-items: center;
  color: yellow;
  margin: 0;
  padding: 0;
  background-color: #000;
}
@media (max-width: 1200px) {
  .map {
    margin-bottom: 3%;
  }
}
</style>
