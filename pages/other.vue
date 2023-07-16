<template>
  <div class="">
    <div class="brr" />
    <div class="photo-man">
      <div class="photo-item">
        <div class="header-photo">
          "อื่นๆ"
        </div>
      </div>
      <br>
      <div v-if="light00" class="photo-item infor_main light00">

        <svg viewBox="25 25 50 50">
          <circle r="20" cy="50" cx="50"></circle>
        </svg>
      </div>
      <div class="photo-item infor_main ">
        <div class="import">
          <div class="coolinput">
            <label for="input" class="text">ขา:</label>
            <input v-model="data.data1" type="number" placeholder="Write here..." class="input">
            <button @click="data.data1 = data.data1 +++ 1">+</button>
            <button @click="data.data1 = data.data1 --- 1">-</button>
            <button @click="data.data1 = 0">X</button>
          </div>
          <br>
          <div class="coolinput">
            <label for="input" class="text">ชั้น:</label>
            <input v-model="data.data2" type="number" placeholder="Write here..." class="input">
            <button @click="data.data2 = data.data2 +++ 1">+</button>
            <button @click="data.data2 = data.data2 --- 1">-</button>
            <button @click="data.data2 = 0">X</button>
          </div>
          <br>
          <div class="coolinput">
            <label for="input" class="text">เศษ:</label>
            <input v-model="data.data3" type="number" placeholder="Write here..." class="input">
            <button @click="data.data3 = data.data3 +++ 1">+</button>
            <button @click="data.data3 = data.data3 --- 1">-</button>
            <button @click="data.data3 = 0">X</button>
          </div>
          <br>
          <div class="import">
            ในเลท มี : {{ sum44 }} ล่อง 
            <br>
            <div class="coolinput">
              <label for="input" class="text">จํานวนชิ้น ในล่อง:</label>
              <input v-model="data.data4" type="number" placeholder="Write here..." class="input">
              <button @click="data.data4 = data.data4 +++ 1">+</button>
              <button @click="data.data4 = data.data4 --- 1">-</button>
              <button @click="data.data4 = 0">X</button>
            </div>
            ในเลท มี : {{ sum33 }} ชิ้น
            <button @click="scum_T()">X</button>
          </div>




        </div>


      </div>
    </div>
  </div>
</template>
  
<script>
export default {
  data() {
    return {
      light00: true,
      number: '',
      data: {
        data1: '',
        data2: '',
        data3: '',
        data4: ''
      },
      sum33: '',
      sum44: ''

    }
  },
  methods: {
    add_number() {
      this.number = 1 + 1
    },
    scum_T() {
    var A1 = this.data.data1
    var A2 = this.data.data2
    var A3 = this.data.data3
    var A4 = this.data.data4

      
      var A = A1 * A2
      var B = A3 +++ A
      var C = B * A4
      this.sum44 = B
      this.sum33 = C
      
    },
    light002() {
      setTimeout(() => {
        this.light00 = false
      }, 1000);
    }
  },
  mounted() {
    this.light002();
    setInterval(() => {
      this.scum_T()
    }, 5000);
  },
  watch: {

  }
}
</script>
  
<style>
.light00 svg {
  width: 3.25em;
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

.import {
  display: flex;
  width: 100%;
  flex-direction: column;
  align-items: center;

}

.import .coolinput {
  display: flex;
  flex-direction: column;
  width: 75%;
  position: static;
  flex-direction: row;

}

.import .coolinput label.text {
  font-size: 0.75rem;
  color: #818df8;
  font-weight: 700;
  position: absolute;
  /* top: 30%; */
  height: 10px;
  left: 5px;
  margin: 0 0 0 7px;
  padding: 0 3px;
  background: #ffffff;
  width: -moz-fit-content;
  width: fit-content;
}

.import .coolinput input[type=number].input {
  padding: 11px 10px;
  font-size: 0.75rem;
  border: 2px #818CF8 solid;
  border-radius: 5px;
  width: 100%;
  background: #e8e8e854;
}

.import .coolinput input[type=number].input:focus {
  outline: none;
}

.import button {
  width: 20%;
  border: 2px #818CF8 solid;
  border-radius: 5px;
}
</style>