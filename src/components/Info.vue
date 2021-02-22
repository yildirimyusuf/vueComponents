<template>
  <div class="info" :class="Style">
    <div class="info-icon" v-if="Icon">
      <img alt="info-img" :src="getImgUrl(pic)" style="width: 30px;">
    </div>
    <div class="info-content">
      <h1 class="info-header" v-if="Header">{{ Header }}</h1>
      <h3 class="info-text" v-if="Text">{{ Text }}</h3>
    </div>
  </div>
</template>

<script>

export default {
  props: [
    'Header',
    'Text',
    'Style',
    'Border',
    'FontType',
    'Icon'
  ],
  methods:{
    getImgUrl() {
    var images = require.context('../assets/', false, /\.png$/)
    return images('./' + this.Icon + ".png")
    }
  }
}
</script>

<style scoped>
.info {
  width: 40%;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 30px;
  margin-left: 50px ;
  border-radius: 25px;
  margin-top: 50px;

}
.info-icon {
  width: 20%;
}
.info-content {
  width: 80%;
}
.info-content .info-header {
  color:black;
}
.info-content .info-text {
  color:black;
}
.info.blue-info {
  background: lightskyblue;
  border: black;
  color: blue;
}
.info.green-info {
  background: palegreen;
  border: black;
  color: green;
}
.info.yellow-info {
  background: rgb(199, 199, 92);
  border: black;
  color: black;
}
.info.red-info {
  background: rgb(224, 107, 107);
  border: black;
  color: red;
}
</style>