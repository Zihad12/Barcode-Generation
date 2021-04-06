<template>
  <div id="app">
    <div>
      <label for="code">Code</label>
      <input type="text" placeholder="Enter code" v-model="code" />
    </div>
    <div>
      <label for="height">Height</label>
      <select v-model="height">
        <option value="50">50</option>
        <option value="100">100</option>
      </select>

      <div>
        <label for="">Font Size</label>
        <select v-model="font_size" name="" id="">
          <option value="10">10</option>
          <option value="15">15</option>
          <option value="20">20</option>
          <option value="40">40</option>
        </select>
      </div>

      <div>
        <label for="">Width</label>
        <select v-model="width" name="" id="">
          <option value="1">1</option>
          <option value="1.5">1.5</option>
          <option value="2">2</option>
          <option value="3">3</option>
          <option value="4">4</option>
        </select>
      </div>
    </div>
    <barcode
      v-model="code"
      v-bind:fontSize="font_size"
      v-bind:height="height"
      v-bind:text="code"
      v-bind:width="width"
    ></barcode>
  </div>
</template>

<script>
import VueBarcode from "vue-barcode";

export default {
  // import {  } from "module";
  components: {
    barcode: VueBarcode,
  },
  data() {
    return {
      code: "lorem ipsum",
      height: 100,
      font_size: 20,
      width : 1,
      text : "WellMax Value"
    };
  },
  methods: {},
  computed: {},
};
</script>

<style scoped></style>
