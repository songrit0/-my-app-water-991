<template>
  <div class="">
    <div class="brr" />
    <div class="photo-man">
      <div class="photo-item">
        <div class="header-photo">
          "ระบบคิดค่าน้ำ"
        </div>
      </div>
      <div class="photo-item infor_main">
        <div class="main_menu">
          <div class="menuitem menuitem_headr">
            <li><svg  xmlns="http://www.w3.org/2000/svg" width="70" height="70" fill="#fff" class="bi bi-person-vcard" viewBox="0 0 16 16">
              <path d="M5 8a2 2 0 1 0 0-4 2 2 0 0 0 0 4Zm4-2.5a.5.5 0 0 1 .5-.5h4a.5.5 0 0 1 0 1h-4a.5.5 0 0 1-.5-.5ZM9 8a.5.5 0 0 1 .5-.5h4a.5.5 0 0 1 0 1h-4A.5.5 0 0 1 9 8Zm1 2.5a.5.5 0 0 1 .5-.5h3a.5.5 0 0 1 0 1h-3a.5.5 0 0 1-.5-.5Z"/>
              <path d="M2 2a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V4a2 2 0 0 0-2-2H2ZM1 4a1 1 0 0 1 1-1h12a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1H8.96c.026-.163.04-.33.04-.5C9 10.567 7.21 9 5 9c-2.086 0-3.8 1.398-3.984 3.181A1.006 1.006 0 0 1 1 12V4Z"/>
            </svg></li>
            <div class="main_menu">
              <li>User : songrit data </li>
              <li>ID : user#1234</li>
            </div>
          </div>
          <div class="menuitem">
            <li>คิดค่าน้ำ</li>
          </div>
          <div class="menuitem">
            <li>ข้อมูล บ้าน</li>
          </div>
          <div class="menuitem">
            <li>อื่นๆ</li>
          </div>
          <div class="menuitem">
            <li>จัดการบัญชี</li>
          </div>
         
        </div>

      </div>
      <br>
      <br>
      <br>
      <br>
      <br>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {

    }

  },
  methods: {

  },
}
</script>

<style>
.main_menu {
  display: grid;
  width: 90%;
  border-radius: 10px 10px 0px 0px;
  background-color: #9B2FDA;
}
.menuitem:hover{
  background-color: #00000025;
}
.menuitem {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: row;
  height: 70px;
  border-bottom: 2px solid #ffffff;
}

.menuitem li {
  color: black;
  font-size: 20px;
  display: grid;
  color: #ffffff;
  text-shadow: 4px 3px 6px rgba(13, 13, 13, 0.8);
}

.menuitem_headr {
  background-color: #f39200;
  border-radius: 10px 10px 0px 0px;
  height: 90px;
  display: flex;
  justify-content: flex-start;
  padding: 10px;
}
.menuitem_headr .main_menu{
  background-color: #ffffff00;
 padding: 20px;

}

</style>