<template>
  <div id="app" data-app>
    <div class="row justify-content-between align-items-center">
      <div class="col-auto px-0">
        <h2>
          To do list
        </h2>
      </div>
     <div class="col-auto px-0">
       <div class="circle" @click="showPopupMain">
         <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20" fill="none">
           <rect x="9" width="2" height="20" fill="#314B99"/>
           <rect x="20" y="9" width="2" height="20" transform="rotate(90 20 9)" fill="#314B99"/>
         </svg>
       </div>
     </div>

    </div>
    <div class="row">
      <search-input ></search-input>
    </div>
    <div class="popup" v-if="togglePopup">
      <div class="popup_main">
        <div class="row popup_main-row-title align-items-center justify-content-between">
          <div class="col-auto p-0"><h3>Создать новую задачу</h3></div>

          <div class="popup_close col-auto px-0 p-0" @click="hidePopupMain">
            <svg xmlns="http://www.w3.org/2000/svg" width="8" height="8" viewBox="0 0 8 8" fill="none">
              <path d="M1 1L4 4M7 7L4 4M4 4L7 1M4 4L1 7" stroke="white" stroke-linecap="round"/>
            </svg>
          </div>
        </div>
        <div class="row">
          <p class="px-0">
            Описание
          </p>
        </div>
        <div class="row">
          <input type="text" placeholder="Введите описание">
        </div>
        <div class="row justify-content-center">
          <button>Создать</button>
        </div>
      </div>
  </div>
  </div>


</template>

<script>
import searchInput from "@/components/searchInput";
 export default {
  name: 'App',
  components: {searchInput},
   data(){
return{
  togglePopup:false
}


   },
methods:{
  showPopupMain(){
      this.togglePopup=true
  },
  hidePopupMain(){
      this.togglePopup=false
  }
}

}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@700&display=swap');
$light_violet: #D6DBEB;
$hover_light_violet:#9497a2;

$blue:#314B99;
$hover_blue: #4c7cfa;

$light_blue:#F0F5FF;
$hover_light_blue: #b0ceff;
*{
  transition: 0.2s;
  outline: none;
}
#app {
  padding-top: 104px;
  max-width: 1300px;
  width: 100%;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  & .row{
    padding: 0;
    margin: 0;
  }
}
.px-0{
  padding-left: 0!important;
  padding-right: 0!important;
}
h2 {
  font-family: 'Montserrat', sans-serif;
  font-size: 24px!important;
  width: auto;
  letter-spacing: 0em;
  text-align: left;
}
h3{
   font-family: Montserrat;
  font-size: 18px!important;
  font-weight: 700 !important;
    text-align: left;
  margin: 0 !important;

}
p{
  font-family: VelaSans;color: #16191D;
  font-weight: 400;
  font-size: 14px!important;
  margin-bottom: 5px;
}
.circle{
  width: 40px;
  height: 40px;
  padding: 0;
  margin: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  background-color:  $light_violet;
  &:hover{
    background-color: $hover_light_violet;
    cursor: pointer;
  }
}
.popup{
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  background: rgba(255, 255, 255, 0.01);
  backdrop-filter: blur(4px);
  display: flex;
  justify-content: center;align-items: center;
  &_main{
    background: #FFFFFF;
    width: 100%;
    max-width: 400px;
    border: 1px solid #DDE2E4;
    padding: 40px;
    box-shadow: 0px 25px 50px -12px rgba(0, 0, 0, 0.25);
    border-radius: 6px;
    &-row-title{
      margin-bottom: 30px!important;
    }
  }
  &_close{
    background:$blue ;
    border-radius: 5px;
    width: 22px!important;
    display: flex;
    justify-content: center;align-items: center;
    height: 22px;
    &:hover{
      background-color: $hover_blue;
      cursor: pointer;
    }
  }
  & input{
    width: 100%;
    background-color: transparent;
    border: 1px solid #DDE2E4;
    border-radius: 8px;
    height: 40px;
    margin-bottom: 30px;
  }
  & button{
    color: $blue;
    padding: 12px 40px;
    background-color:$light_blue;
    border-radius: 8px;
    max-width: 150px;
    margin-bottom: 10px;
    &:hover{
      background-color: $hover_light_blue;
      color: white;
    }

  }

}
</style>
