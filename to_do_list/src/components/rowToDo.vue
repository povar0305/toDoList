<template>
  <div class="row tabelList_info ">
    <div class="tabelList_info-check">
      <v-checkbox
          v-model="result"
      ></v-checkbox>
    </div>
    <div class="tabelList_info-name">
      Описание
    </div>
    <div class="tabelList_info-status">
      Статус
    </div>
    <div class="tabelList_info-date">
      Дата
    </div>
  </div>
</template>

<script>
export default {
  name: "rowToDo",
  data () {
    return {
      result: false,
    }
  },
}
</script>

<style scoped lang="scss">
.tabelList_info {
  padding-bottom: 20px!important;
  padding-top: 20px!important;
  &:hover{
    background-color:  #F6F9FF;
  }
  & .v-input--selection-controls{
    padding-top: 0!important;
    margin-top: 0!important;
  }
  & > * {
    font-family: VelaSans;
    color: #16191D;
    font-weight: 400;
    font-size: 14px;
  }

  &-check {
    border-right: 1px solid #C4C4C4;
    width: 10%;
    height: 100%;
    display: flex;
    justify-content: center;align-items: center;

  }

  &-date, &-status {
    width: 15%;
    border-left: 1px solid #C4C4C4;
  }

  &-name {
    width: 60%;
  }
}
</style>