<template>
  <v-row class="justify-center align-items-center">
    <v-col class="p-0">
      Сортировать по :

    </v-col>
    <v-col class="p-0">
      <v-select
          @input="sortBy"
          :items="items"
          label="Дате"
          solo
          return-object
      ></v-select>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "selectSort",
  data() {
    return {
      items: ['Дате', 'Статусу'],
    }
  },
  methods:{
    sortBy(item){
      console.log(item) //получили то, по чему сортировать
    }
  }
}
</script>

<style   lang="scss">
.v-text-field, .v-input__slot {
  padding: 0px;
  margin: 0px;
}

.v-text-field__details {
  display: none !important;
}

.v-text-field > .v-input__control > .v-input__slot:before, .v-text-field > .v-input__control > .v-input__slot:after {
  border: none !important;
}

.v-text-field.v-text-field--solo:not(.v-text-field--solo-flat) > .v-input__control > .v-input__slot {
  box-shadow: none !important;
}
</style>