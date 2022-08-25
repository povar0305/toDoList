<template>
<div class="row tabelList">
  <div class="row tabelList_title">
    <div class="tabelList_check">

    </div>
    <div class="tabelList_name">
      Описание
    </div>
    <div class="tabelList_status">
      Статус
    </div>
    <div class="tabelList_date">
      Дата
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: "tabelList"
}
</script>

<style scoped lang="scss">
.tabelList{
  &>*{
    font-family: VelaSans;
    color: #16191D;
    font-weight: 400;
    font-size: 14px;
  }
  &_check{
    border-right: 1px solid #C4C4C4;
    width: 10%;
    height: 100%;
  }
  &_date,&_status{
    width: 15%;
    border-left: 1px solid #C4C4C4;
  }
  &_name{
    width: 60%;
  }
}
</style>