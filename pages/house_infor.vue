<template>
  <div class="">
    <div class="brr" />
    <div class="photo-man">
      <div class="photo-item">
        <div class="header-photo">
          "หน้าข้อมูลบ้าน"
        </div>
      </div>
      <br>
      <div class="photo-item infor_main">
        <div class="infor_item">
          <div class="infor_item_row">

            <form class="form">
              <button>
                <svg width="17" height="16" fill="none" xmlns="http://www.w3.org/2000/svg" role="img"
                  aria-labelledby="search">
                  <path d="M7.667 12.667A5.333 5.333 0 107.667 2a5.333 5.333 0 000 10.667zM14.334 14l-2.9-2.9"
                    stroke="currentColor" stroke-width="1.333" stroke-linecap="round" stroke-linejoin="round"></path>
                </svg>
              </button>
              <input class="input" placeholder="Type your text" required="" type="text">
              <button class="reset" type="reset">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
                  stroke="currentColor" stroke-width="2">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"></path>
                </svg>
              </button>
            </form>

          </div>
          <div class="infor_item_row">

            <button class="button">
              <svg xmlns="http://www.w3.org/2000/svg" width="20" viewBox="0 0 20 20" height="20" fill="none"
                class="svg-icon">
                <g stroke-width="1.5" stroke-linecap="round" stroke="#812a0d">
                  <circle r="2.5" cy="10" cx="10"></circle>
                  <path fill-rule="evenodd"
                    d="m8.39079 2.80235c.53842-1.51424 2.67991-1.51424 3.21831-.00001.3392.95358 1.4284 1.40477 2.3425.97027 1.4514-.68995 2.9657.82427 2.2758 2.27575-.4345.91407.0166 2.00334.9702 2.34248 1.5143.53842 1.5143 2.67996 0 3.21836-.9536.3391-1.4047 1.4284-.9702 2.3425.6899 1.4514-.8244 2.9656-2.2758 2.2757-.9141-.4345-2.0033.0167-2.3425.9703-.5384 1.5142-2.67989 1.5142-3.21831 0-.33914-.9536-1.4284-1.4048-2.34247-.9703-1.45148.6899-2.96571-.8243-2.27575-2.2757.43449-.9141-.01669-2.0034-.97028-2.3425-1.51422-.5384-1.51422-2.67994.00001-3.21836.95358-.33914 1.40476-1.42841.97027-2.34248-.68996-1.45148.82427-2.9657 2.27575-2.27575.91407.4345 2.00333-.01669 2.34247-.97026z"
                    clip-rule="evenodd"></path>
                </g>
              </svg>
              <span class="lable">ค้นหา</span>
            </button>

          </div>
        </div>
        <div class="infor_item">
          <div class="home_item">
            <div class="infor_item">
              <div class="infor_item_row">
                <h1>1324/11</h1>
                <h3><b>songrit</b></h3>
              </div>
              <div class="infor_item_row">
                <div class="infor_item">
                  <svg xmlns="http://www.w3.org/2000/svg" width="50" fill="currentColor" class="bi bi-cash-coin"
                    viewBox="0 0 16 16">
                    <path fill-rule="evenodd"
                      d="M11 15a4 4 0 1 0 0-8 4 4 0 0 0 0 8zm5-4a5 5 0 1 1-10 0 5 5 0 0 1 10 0z" />
                    <path
                      d="M9.438 11.944c.047.596.518 1.06 1.363 1.116v.44h.375v-.443c.875-.061 1.386-.529 1.386-1.207 0-.618-.39-.936-1.09-1.1l-.296-.07v-1.2c.376.043.614.248.671.532h.658c-.047-.575-.54-1.024-1.329-1.073V8.5h-.375v.45c-.747.073-1.255.522-1.255 1.158 0 .562.378.92 1.007 1.066l.248.061v1.272c-.384-.058-.639-.27-.696-.563h-.668zm1.36-1.354c-.369-.085-.569-.26-.569-.522 0-.294.216-.514.572-.578v1.1h-.003zm.432.746c.449.104.655.272.655.569 0 .339-.257.571-.709.614v-1.195l.054.012z" />
                    <path
                      d="M1 0a1 1 0 0 0-1 1v8a1 1 0 0 0 1 1h4.083c.058-.344.145-.678.258-1H3a2 2 0 0 0-2-2V3a2 2 0 0 0 2-2h10a2 2 0 0 0 2 2v3.528c.38.34.717.728 1 1.154V1a1 1 0 0 0-1-1H1z" />
                    <path d="M9.998 5.083 10 5a2 2 0 1 0-3.132 1.65 5.982 5.982 0 0 1 3.13-1.567z" />
                  </svg>
                </div>
                <h3><b>เดือนล่าสุด : 000 ฿</b></h3>
              </div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>
  
<script>
export default {

}
</script>
  
<style>
.infor_item {
  display: flex;
  justify-content: space-around;
  width: 100%;
  height: auto;
  align-items: flex-start;
  flex-direction: row;
}

.infor_item_row {
  display: grid;
  width: 50%;
  height: 100%;
  justify-content: center;
  margin: 10px;
}

.home_item {
  border-radius: 12px;
  border: 1px solid #FF5117;
  width: 80%;
  height: auto;
  margin: 30px;
}

/* From uiverse.io by @satyamchaudharydev */
/* removing default style of button */

.infor_item_row .form button {
  border: none;
  background: none;
  color: #8b8ba7;
}

/* styling of whole input container */
.infor_item_row .form {
  --timing: 0.3s;
  --width-of-input: 200px;
  --height-of-input: 40px;
  --border-height: 2px;
  --input-bg: #fff;
  --border-color: #FF5117;
  --border-radius: 10px;
  --after-border-radius: 1px;
  position: relative;
  width: var(--width-of-input);
  height: var(--height-of-input);
  display: flex;
  align-items: center;
  padding-inline: 0.8em;
  border-radius: var(--border-radius);
  transition: border-radius 0.5s ease;
  background: var(--input-bg, #fff);
  border: 1px solid #FF5117;
}

/* styling of Input */
.infor_item_row .input {
  font-size: 0.9rem;
  background-color: transparent;
  width: 100%;
  height: 100%;
  padding-inline: 0.5em;
  padding-block: 0.7em;
  border: none;
}

/* styling of animated border */
.infor_item_row .form:before {
  content: "";
  position: absolute;
  background: var(--border-color);
  transform: scaleX(0);
  transform-origin: center;
  width: 100%;
  height: var(--border-height);
  left: 0;
  bottom: 0;
  border-radius: 1px;
  transition: transform var(--timing) ease;
}

/* Hover on Input */
.infor_item_row .form:focus-within {
  border-radius: var(--after-border-radius);
}

.infor_item_row input:focus {
  outline: none;
}

/* here is code of animated border */
.infor_item_row .form:focus-within:before {
  transform: scale(1);
}

/* styling of close button */
/* == you can click the close button to remove text == */
.reset {
  border: none;
  background: none;
  opacity: 0;
  visibility: hidden;
}

/* close button shown when typing */
.infor_item_row input:not(:placeholder-shown)~.reset {
  opacity: 1;
  visibility: visible;
}

/* sizing svg icons */
.infor_item_row .form svg {
  width: 17px;
  margin-top: 3px;
}

.infor_item_row .button {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 6px 12px;
  gap: 8px;
  height: 36px;
  width: 120px;
  border: none;
  background: #FF5117;
  border-radius: 20px;
  cursor: pointer;
}

.infor_item_row .lable {
  line-height: 20px;
  font-size: 17px;
  color: #fcc2af;
  font-family: sans-serif;
  letter-spacing: 1px;
}

.infor_item_row .button:hover {
  background: #FF5117;
}

.infor_item_row .button:hover .svg-icon {
  animation: spin 2s linear infinite;
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
  }
}</style>