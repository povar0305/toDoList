<template>
  <div id="app" data-app>
    <div class="row justify-content-between align-items-center">
      <div class="col-auto">
        <h2>
          To do list
        </h2>
      </div>
     <div class="col-auto">
       <div class="circle">
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
  </div>
</template>

<script>
import searchInput from "@/components/searchInput";
export default {
  name: 'App',
  components: {searchInput},


}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@700&display=swap');
$light_violet: #D6DBEB;
$hover_light_violet:#9497a2;
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

h2 {
  font-family: 'Montserrat', sans-serif;
  font-size: 24px!important;
  width: auto;
  letter-spacing: 0em;
  text-align: left;
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
</style>
