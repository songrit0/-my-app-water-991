<template lang="">
    <div style="">  
      <div class="Fullscreen ">
        <button @click="closeFullscreen()" class="on_closeFullscreen"><svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="#DBDBDB" class="bi bi-fullscreen-exit" viewBox="0 0 16 16">
          <path d="M5.5 0a.5.5 0 0 1 .5.5v4A1.5 1.5 0 0 1 4.5 6h-4a.5.5 0 0 1 0-1h4a.5.5 0 0 0 .5-.5v-4a.5.5 0 0 1 .5-.5zm5 0a.5.5 0 0 1 .5.5v4a.5.5 0 0 0 .5.5h4a.5.5 0 0 1 0 1h-4A1.5 1.5 0 0 1 10 4.5v-4a.5.5 0 0 1 .5-.5zM0 10.5a.5.5 0 0 1 .5-.5h4A1.5 1.5 0 0 1 6 11.5v4a.5.5 0 0 1-1 0v-4a.5.5 0 0 0-.5-.5h-4a.5.5 0 0 1-.5-.5zm10 1a1.5 1.5 0 0 1 1.5-1.5h4a.5.5 0 0 1 0 1h-4a.5.5 0 0 0-.5.5v4a.5.5 0 0 1-1 0v-4z"/>
        </svg> </button>
        <button @click="openFullscreen()" class="off_closeFullscreen" ><svg xmlns="http://www.w3.org/2000/svg" width="30" height="30"  fill="#DBDBDB" class="bi bi-fullscreen" viewBox="0 0 16 16">
          <path d="M1.5 1a.5.5 0 0 0-.5.5v4a.5.5 0 0 1-1 0v-4A1.5 1.5 0 0 1 1.5 0h4a.5.5 0 0 1 0 1h-4zM10 .5a.5.5 0 0 1 .5-.5h4A1.5 1.5 0 0 1 16 1.5v4a.5.5 0 0 1-1 0v-4a.5.5 0 0 0-.5-.5h-4a.5.5 0 0 1-.5-.5zM.5 10a.5.5 0 0 1 .5.5v4a.5.5 0 0 0 .5.5h4a.5.5 0 0 1 0 1h-4A1.5 1.5 0 0 1 0 14.5v-4a.5.5 0 0 1 .5-.5zm15 0a.5.5 0 0 1 .5.5v4a1.5 1.5 0 0 1-1.5 1.5h-4a.5.5 0 0 1 0-1h4a.5.5 0 0 0 .5-.5v-4a.5.5 0 0 1 .5-.5z"/>
        </svg> </button>
        <button class="back" @click="GO0() " v-if="pages_check()">กลับ</button>
      </div>   
<div class="header">
    <a @click="pages_les = 'Home',goto('/')" class="active text-fff header-item" ><svg xmlns="http://www.w3.org/2000/svg" :width="svg_z.width" :height="svg_z.height" fill="currentColor" class="z-index-2 bi bi-house" viewBox="0 0 16 16">
  <path d="M8.707 1.5a1 1 0 0 0-1.414 0L.646 8.146a.5.5 0 0 0 .708.708L2 8.207V13.5A1.5 1.5 0 0 0 3.5 15h9a1.5 1.5 0 0 0 1.5-1.5V8.207l.646.647a.5.5 0 0 0 .708-.708L13 5.793V2.5a.5.5 0 0 0-.5-.5h-1a.5.5 0 0 0-.5.5v1.293L8.707 1.5ZM13 7.207V13.5a.5.5 0 0 1-.5.5h-9a.5.5 0 0 1-.5-.5V7.207l5-5 5 5Z"/>
</svg><p class="z-index-2">{{textbar[0]}}</p><div  class="raddot z-index-1" v-if="pages_les == 'Home'"/></a>
    <a @click="pages_les = 'Contact',goto('/house_infor')" class="active text-fff header-item" >
<svg xmlns="http://www.w3.org/2000/svg" :width="svg_z.width" :height="svg_z.height" fill="currentColor" class="z-index-2 bi bi-archive" viewBox="0 0 16 16">
  <path d="M0 2a1 1 0 0 1 1-1h14a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1v7.5a2.5 2.5 0 0 1-2.5 2.5h-9A2.5 2.5 0 0 1 1 12.5V5a1 1 0 0 1-1-1V2zm2 3v7.5A1.5 1.5 0 0 0 3.5 14h9a1.5 1.5 0 0 0 1.5-1.5V5H2zm13-3H1v2h14V2zM5 7.5a.5.5 0 0 1 .5-.5h5a.5.5 0 0 1 0 1h-5a.5.5 0 0 1-.5-.5z"/>
</svg>
      <p class="z-index-2">{{textbar[1]}}</p>
      <div  class="raddot z-index-1" v-if="pages_les == 'Contact'"/></a>
    <a  @click="pages_les = 'export',goto('/charge')" class="active text-fff header-item" ><svg xmlns="http://www.w3.org/2000/svg" :width="svg_z.width" :height="svg_z.height" fill="currentColor" class="z-index-2 bi bi-explicit" viewBox="0 0 16 16">
  <path d="M6.826 10.88H10.5V12h-5V4.002h5v1.12H6.826V7.4h3.457v1.073H6.826v2.408Z"/>
  <path d="M2.5 0A2.5 2.5 0 0 0 0 2.5v11A2.5 2.5 0 0 0 2.5 16h11a2.5 2.5 0 0 0 2.5-2.5v-11A2.5 2.5 0 0 0 13.5 0h-11ZM1 2.5A1.5 1.5 0 0 1 2.5 1h11A1.5 1.5 0 0 1 15 2.5v11a1.5 1.5 0 0 1-1.5 1.5h-11A1.5 1.5 0 0 1 1 13.5v-11Z"/>
</svg><p class="z-index-2">{{textbar[2]}}</p><div  class="raddot z-index-1" v-if="pages_les == 'export'"/></a>
    <a @click="pages_les = 'About',goto('/other')" class="active text-fff header-item" ><div  class="raddot z-index-1" v-if="pages_les == 'About'"/><svg xmlns="http://www.w3.org/2000/svg" :width="svg_z.width" :height="svg_z.height" fill="currentColor" class="z-index-2 bi bi-file-earmark-person" viewBox="0 0 16 16">
  <path d="M11 8a3 3 0 1 1-6 0 3 3 0 0 1 6 0z"/>
  <path d="M14 14V4.5L9.5 0H4a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2zM9.5 3A1.5 1.5 0 0 0 11 4.5h2v9.255S12 12 8 12s-5 1.755-5 1.755V2a1 1 0 0 1 1-1h5.5v2z"/>
</svg><p class="z-index-2">{{textbar[3]}}</p></a>
</div>

    </div>
</template>
<script>
import { useRoute } from 'vue-router'
export default {
  data() {
    return {
      svg_z: { width: 30, height: 30 },
      pages_les: '',
      textbar: ['หน้าหลัก', 'ข้อมูล', 'คิดค่าน้ำ', 'อื่นๆ']
    }
  },
  methods: {
    GO0() {
      this.$router.go(-1)
      setTimeout(() => {
        this.get_router_push()
      }, 100);

    },
    goto(item) {
      this.$router.push(item)
    },
    openFullscreen() {
      var elem = document.documentElement;
      if (elem.requestFullscreen) {
        elem.requestFullscreen();
      } else if (elem.webkitRequestFullscreen) {
        elem.webkitRequestFullscreen();
      } else if (elem.msRequestFullscreen) {
        elem.msRequestFullscreen();
      }
    },
    closeFullscreen() {
      if (document.exitFullscreen) {
        document.exitFullscreen();
      } else if (document.webkitExitFullscreen) {
        document.webkitExitFullscreen();
      } else if (document.msExitFullscreen) {
        document.msExitFullscreen();
      }
    },
    get_router_push() {
      var path = this.$route.path
      if (path == '/house_infor') {
        console.log(`mypath : house_infor`);
        this.pages_les = 'Contact'
      } else if (path == '/charge') {
        console.log(`mypath : charge`);
        this.pages_les = 'export'
      } else if (path == '/other') {
        console.log(`mypath : other`);
        this.pages_les = 'About'
      } else {
        console.log(`mypath : null`);
        this.pages_les = 'Home'
      }
    },
    pages_check(){
      var path = this.$route.path 
      if (path == '/') {
        return false
      } else {
        return true
      }
    }
  },
  mounted() {
    
    this.get_router_push()
    console.log(this.$route.path);
  },

}
</script>
<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}

.active {
  width: 100%;
  height: 200%;
}

.header {
  display: flex;
  overflow: hidden;
  background-color: #0C0C0C;
  padding: 19px 43px;
  flex-direction: row;
  height: 82px;
  align-items: center;
  justify-content: center;
  column-gap: 35px;
}

.text-fff {
  color: #fff;
}

.header-item {
  display: grid;
  align-content: center;
  justify-content: center;
  justify-items: center;

}

.raddot {
  border-radius: 15px 15px 5px 5px;
  background-color: rgba(158, 158, 158, 0.459);
  width: 76px;
  height: 76px;
  position: fixed;
  bottom: -100px;
  animation: slide-top 0.5s cubic-bezier(0.48, -0.81, 0.4, 1.5) both;
}


@-webkit-keyframes slide-top {
  0% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }

  100% {
    -webkit-transform: translateY(-100px);
    transform: translateY(-100px);
  }
}

@keyframes slide-top {
  0% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }

  100% {
    -webkit-transform: translateY(-100px);
    transform: translateY(-100px);
  }
}

.z-index-1 {
  z-index: 1;
}

.z-index-2 {
  z-index: 2;
}

/* @media screen and (max-width: 500px) {
  .header a {
    float: none;
    display: block;
    text-align: left;
  }
  
  .header-right {
    float: none;
  }
} */
.Fullscreen {
  display: flex;
  justify-content: space-between;

}

.Fullscreen .back {
  position: fixed;
  left: 85%;
  color: red;
  border: 1px solid red;
}

.Fullscreen button {
  --border-radius: 25px;
  --border-width: 7px;
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  position: relative;
  border: 0;
  background-color: #ffffff;
  font-size: 18px;
  font-weight: 500;
  color: rgba(255, 255, 255, 1);
  position: fixed;
  bottom: 85px;
  left: 5px;
  display: flex;
  border-radius: 40px;
  width: 47px;
  height: 47px;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  border: 1px solid #999999;
}

:fullscreen .Fullscreen .on_closeFullscreen {
  display: flex;

}

:fullscreen .Fullscreen .off_closeFullscreen {
  display: none;

}
</style>