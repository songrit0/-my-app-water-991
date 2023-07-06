<template>
  <div class="layouts">
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
      cars : '1'
    }
  },
  methods: {
    addback(item) {
      var m = 'background-color:'
      return m + item
    },

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
</style>