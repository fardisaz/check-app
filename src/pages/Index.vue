<template>
  <q-page class="flex flex-center">
    <div id="q-app">
  <div class="q-pa-md">

    <div v-for="arr in myArray" :key="arr.bgColor" class="q-pa-sm flex">
      <q-checkbox
        v-model="arr.checked"
        keep-color
        :label="arr.name"
        :style="{ color: '#' + arr.bgColor }"
      ></q-checkbox>
    </div>

  </div>
</div>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data() {
    return {
      myArray: [
        {
          bgColor: "501253",
          checked: false,
          name:"first"
        },
        {
          bgColor: "acedef",
          checked: false,
          name:"second"
        },
        {
          bgColor: "deadbeef",
          checked: false,
          name:"third"
        },
        {
          bgColor: "linear-gradient(90deg,#f24949 25%,#f2cf00 0,#f2cf00 50%,#8bd12a 0,#8bd12a 75%,#36c 0)",
          checked: false,
          name:"fourth"
        }
      ]
    };
  }
}
</script>
<style scoped>
.q-checkbox >>> .q-checkbox__inner {
  color: unset;
}
.q-checkbox >>> .q-checkbox__label {
  color: black;
}
.q-checkbox >>> .q-checkbox__inner .q-checkbox__bg {
  background: currentColor;
}
</style>
