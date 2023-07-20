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

      <div class="photo-item infor_main ">
        <div class="import">


          <div class="grid">
            <div class="item">
              <div class="content">
                <div class="coolinput">
                  <label for="input" class="text">ขา:</label>
                  <input v-model="data.data1" type="number" placeholder="Write here..." class="input">
                  <button @click="data.data1 = data.data1++ + 1, datacheck++ + 1">+</button>
                  <button @click="data.data1 = data.data1-- - 1, datacheck++ + 1">-</button>
                  <button @click="data.data1 = 0, datacheck++ + 1">X</button>
                </div>
              </div>
            </div>
            <div class="item">
              <div class="content">
                <div class="coolinput">
                  <label for="input" class="text">ชั้น:</label>
                  <input v-model="data.data2" type="number" placeholder="Write here..." class="input">
                  <button @click="data.data2 = data.data2++ + 1, datacheck++ + 1">+</button>
                  <button @click="data.data2 = data.data2-- - 1, datacheck++ + 1">-</button>
                  <button @click="data.data2 = 0, datacheck++ + 1">X</button>
                </div>
              </div>
            </div>
            <div class="item">
              <div class="content">
                <div class="coolinput">
                  <label for="input" class="text">เศษ:</label>
                  <input v-model="data.data3" type="number" placeholder="Write here..." class="input">
                  <button @click="data.data3 = data.data3++ + 1, datacheck++ + 1">+</button>
                  <button @click="data.data3 = data.data3-- - 1, datacheck++ + 1">-</button>
                  <button @click="data.data3 = 0, datacheck++ + 1">X</button>
                </div>
              </div>
            </div>
            <div class="item">
              <div class="content">
                <div class="coolinput">
                  <label for="input" class="text" style="color: #fb922c;">จํานวนชิ้น ในกล่อง:</label>
                  <input v-model="data.data4" type="number" placeholder="Write here..." class="input" style="
                  border: 2px #fb922c solid;
              ">
                  <button @click="data.data4 = data.data4++ + 1, datacheck++ + 1" style="
                  border: 2px #fb922c solid;
              ">+</button>
                  <button @click="data.data4 = data.data4-- - 1, datacheck++ + 1" style="
                  border: 2px #fb922c solid;
              ">-</button>
                  <button @click="data.data4 = 0, datacheck++ + 1" style="
                  border: 2px #fb922c solid;
              ">X</button>
                </div>
              </div>
            </div>
          </div>





          <br>

          <br>

          <br>
          <div class="import">
            ในเลท มี : {{ sum44 }} กล่อง
            <br>

            ในเลท มี : {{ sum33 }} ชิ้น
            <!-- <button @click="scum_T()">X</button> -->
      


            <button @click="add_number()">รวม</button>
            <br>






            <div class="grid2">

              <div class="item" v-for="(item, index) in mylogdata" :key="index">
                <div class="content">
                  <div class="content_box">
                    <!-- <p>index:{{ index }} item:{{ item }}</p> -->
                    <p> เลทที่ {{ index + 1 }}</p>
                    <p>ขา:{{ item.data.A1 }}</p>
                    <p>ชั้น:{{ item.data.A2 }}</p>
                    <p> เศษ:{{ item.data.A3 }}</p>
                    <p> ในเลท มี : {{ item.box }} กล่อง</p>
                    <p> ในเลท มี : {{ item.item }} ชิ้น</p>
                    <div class="item">
                      <button @click="number_sum(item.box, index)" :id="`buttonbox-${index}`">รวมเลท</button>
                      <button @click="del(index)">ลบข้อมูล</button>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <br>
            <div class="A1tex">
              <div class="item-row"> รวมเลทในกล่อง มี : {{ sum55 * data.data4 }} ชิ้น \  รวมเลท มี : {{ sum55 }} กล่อง</div>
              <div class="item-row"> รวมเลทบวก : <div style="
                display: flex;
                margin: 0px 0px 0px 7px;
                width: 70%;
                flex-wrap: wrap;
            ">
                <div style="
                margin: 0 0 0 1px;
            " class="" v-for="(item,index) in sum66" :key="item">{{sum66[index]}}</div>{{ sum55 }}</div>
              </div>
            </div>
          </div>


          <br><br><br><br>

        </div>


      </div>
    </div>
  </div>
</template>
  
<script>
export default {
  data() {
    return {

      number: '',
      datacheck: 0,
      data: {
        data1: '',
        data2: '',
        data3: '',
        data4: ''
      },
      sum33: '',
      sum44: '',
      mylogdata: [],
      sum55: '',
      sum66: [],



    }
  },
  methods: {
    del(item) {
      this.mylogdata.splice(item, 1)
    },
    plus(index){

      if (index ==  this.sum66.length) {
        return true
      }
      else {
        return false
      }
    },
    number_sum(item, index) {
      this.sum55 = this.sum55++ + item
      if (this.sum66.length === 0) {
        this.sum66.splice(0,0,`${item}=`)
      } else {
         this.sum66.splice(0,0,`${item}+`)
      }
      console.log(this.sum66);
      
      document.getElementById(`buttonbox-${index}`).style.display = 'none'
    },
    add_number() {
      this.mylogdata.push({ data: { A1: this.data.data1, A2: this.data.data2, A3: this.data.data3, A4: this.data.data4 }, box: this.sum44, item: this.sum33 })
      console.log(this.mylogdata);
    },
    scum_T() {
      var A1 = this.data.data1
      var A2 = this.data.data2
      var A3 = this.data.data3
      var A4 = this.data.data4


      var A = A1 * A2
      var B = A3++ + A
      var C = B * A4
      this.sum44 = B
      this.sum33 = C

    },

  },
  mounted() {

    setInterval(() => {
      this.scum_T()
    }, 5000);
  },
  watch: {
    datacheck() {
      this.scum_T()
    }
  }
}
</script>
  
<style>
.import .grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  justify-items: stretch;
  align-items: stretch;
  grid-column-gap: 20px;
  -moz-column-gap: 20px;
  column-gap: 20px;
  grid-row-gap: 20px;
  row-gap: 20px;
  width: 100%;

}

.import .grid2 {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  justify-items: stretch;
  align-items: stretch;
  grid-column-gap: 20px;
  -moz-column-gap: 20px;
  column-gap: 20px;
  grid-row-gap: 20px;
  row-gap: 20px;
  width: 100%;

}

.grid2 .content_box {
  display: flex;
  border: 2px solid rgb(251, 146, 44);
  height: 160px;
  border-radius: 7px;
  flex-direction: column;
  flex-wrap: nowrap;
}

.grid2 .content_box p {
  display: inline-flex;
  margin: 0px 0 0 4px;
}

.grid2 .content_box .item button {
  width: 40%;
  border: 2px #ec9a00 solid;
  margin: 7px 0 0 3px;
  border-radius: 5px;
  font-size: 10px;
}

.import .content {
  color: #242424;

  font-weight: 600;
  text-align: center;
  box-sizing: border-box;
  height: 100%;
  padding: 10px;
}

.import {
  display: flex;
  width: 100%;
  flex-direction: column;
  align-items: center;

}

.import .coolinput {
  display: flex;
  width: 100%;
  position: static;
  flex-direction: row;
  flex-wrap: wrap;


}

.import .coolinput label.text {
  display: table;
  font-size: 0.75rem;
  color: #818df8;
  font-weight: 700;
  position: absolute;
  /* top: 30%; */
  /* background-position-y: top; */
  /* margin-top: 10px; */
  height: 10px;
  /* left: 5px; */
  margin: -10px 3px -3px 8px;
  padding: 0 3px;
  background: #ffffff;
  width: -moz-fit-content;
  width: fit-content;
}

.import .coolinput .input {
  padding: 11px 10px;
  font-size: 0.75rem;
  border: 2px #818CF8 solid;
  border-radius: 5px;
  width: 100%;
  background: #e8e8e854;
}

.import .coolinput .input:focus {
  outline: none;
}

.import button {
  width: 20%;
  border: 2px #818CF8 solid;
  margin: 7px 0 0 3px;
  border-radius: 5px;
}

.A1tex {
  display: flex;
  flex-direction: column;
  width: 100%;
  margin: 0 0 0 15px;
}

.A1tex .item-row {
  display: flex;
}
</style>