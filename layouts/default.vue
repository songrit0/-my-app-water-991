<template>
  <div class="layouts">
    <div v-if="light00" class="photo-item infor_main light00">
      <svg viewBox="25 25 50 50">
        <circle r="20" cy="50" cx="50"></circle>
      </svg>
    </div>
    <TheHeader class="theheader" />
    <Nuxt style="z-index: 2;" />
    <div class="select" style="z-index: 3;">
      <label for="cars">Choose a car: {{cars}}</label>
      <select name="cars" id="cars" v-model="cars">
        <option value="1">1</option>
        <option value="2">2</option>
       
      </select>
    </div>
    <div class="by" :style="addback(background_theme[1])" />
    <div class="circle" :style="addback(background_theme[0])" />
    <div class="circle5" :style="addback(background_theme[2])" />
    <div class="circlex" :style="addback(background_theme[2])" />
    <div class="circle4" :style="addback(background_theme[2])" />
    <div class="circle2" :style="addback(background_theme[2])" />
    <div class="circle6" :style="addback(background_theme[1])" />
    <div class="circle3" :style="addback(background_theme[1])" />
   

  </div>
</template>
<script>
export default {
  data() {
    return {
      background_theme: ['#4D196B', '#9B2FDA', '#ffffff'],
      cars : '1',
      light00: true,
    }
  },
  methods: {
    addback(item) {
      var m = 'background-color:'
      return m + item
    },
    light002() {
      setTimeout(() => {
        this.light00 = false
      }, 1000);
    }

  },
  mounted() {
    this.light002();
    
  },
  watch: {
    cars(){
      if (this.cars == '1') {
         this.background_theme = ['#4D196B', '#9B2FDA', '#ffffff']
      }
      if (this.cars == '2') {
        this.background_theme = ['#FF5117', '#FF8B00', '#ffffff']
      }
    }
  },
  computed: {},
  components: {}
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Chakra+Petch:wght@300&display=swap');

.layouts {
  display: flex;
  /* position: absolute; */
  flex-direction: column-reverse;
}

* {
  font-family: 'Chakra Petch', sans-serif;
}
p{
  font-size: smaller;
}
.by{
  background-color: blue;
  width: 100%;
  height: 100%;
  position: fixed;
  top: 0;
  left: 0;
 
}
.select {
  display: grid;
  justify-content: end;
  padding: 12px;
  position: fixed;
  top: 0;
  right: 0;
}

.theheader {
  position: fixed;
  z-index: 13;
  width: 100%;
  bottom: 0px;
}

.circle {
  width: 305px;
  height: 305px;
  position: fixed;
  border-radius: 100%;
  top: 16px;
  left: -74px;
}
.circlex{
  width: 305px;
  height: 305px;
  position: absolute;
  border-radius: 100%;
  top: 126px;
  left: 40px;
  z-index: 1;
}
.circle2 {
  width: 380px;
  height: 356px;
  position: fixed;
  border-radius: 100% 132% 45% 50%;
  top: 84px;
  left: -49px;
}

.circle3 {
  width: 108px;
  height: 190px;
  position: fixed;
  border-radius: 97% 100% 54% 100%;
  top: 31px;
  left: 288px;
  transform: rotate(122deg);
}

.circle4 {
  width: 380px;
  height: 356px;
  position: fixed;
  border-radius: 100% 132% 45% 50%;
  top: 140px;
  left: 125px;

}

.circle5 {
  width: 100%;
  height: 100%;
  position: fixed;
  border-radius: 0px;
  top: 172px;
  left: 0px;

}

.circle6 {
  width: 108px;
  height: 190px;
  position: fixed;
  border-radius: 100%;
  top: 44px;
  left: 353px;
  transform: rotate(83deg);
}

 /* main_papges */
.brr {
  height: 150px;
  width: 100%;
}

.photo-man {
  display: grid;
  width: 100%;
  height: auto;

}

.photo-item {
  display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
}

.header-photo {
  display: flex;
  padding: 10px 20px;
  border: none;
  font-size: 17px;
  border-radius: 7px;
  letter-spacing: 4px;
  font-size: 20px;
  color: black;
 /* border-bottom: 1px solid #000000;*/


}

.infor_main {
   background-color: white;
 /*  background-image: linear-gradient(135deg, rgba(155, 47, 218, 1) 18%, rgba(255, 0, 128, 1) 100%);*/
 /*  height: 1000px;*/
  border-radius: 20px 20px 0px 0px;
  padding: 25px 0px;
}

.light00 {
  position: fixed;
    top: 0px;
    z-index: 20;
    width: 100%;
    height: 100%;
    border-radius: 0px;
}
.light00 svg {
  width: 4.25em;
  transform-origin: center;
  animation: rotate4 2s linear infinite;
}

.light00 circle {
  fill: none;
  stroke: hsl(214, 97%, 59%);
  stroke-width: 2;
  stroke-dasharray: 1, 200;
  stroke-dashoffset: 0;
  stroke-linecap: round;
  animation: dash4 1.5s ease-in-out infinite;
}

@keyframes rotate4 {
  100% {
    transform: rotate(360deg);
  }
}

@keyframes dash4 {
  0% {
    stroke-dasharray: 1, 200;
    stroke-dashoffset: 0;
  }

  50% {
    stroke-dasharray: 90, 200;
    stroke-dashoffset: -35px;
  }

  100% {
    stroke-dashoffset: -125px;
  }
}

</style>