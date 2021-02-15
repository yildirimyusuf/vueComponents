<template>
  <div class="container">
    <div class="row">
      <input v-model="dataSource.name" type="text" placeholder="Lütfen İsim Giriniz...">
    </div>
    <div class="row">
      <input v-model="dataSource.surname" type="text" placeholder="Lütfen Soyisim Giriniz...">
    </div>
    <div class="row">
      <input v-model="dataSource.email" type="text" placeholder="Lütfen E-Mail Giriniz...">
    </div>
    <div class="row">
      <button @click="gonder" class="btn btn-primary">Gönder</button>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      dataSource : {
        name : '',
        surname : '',
        email : ''
      }
    }
  },
  methods : {
    gonder(){
      this.$emit("dataSource", this.dataSource)
    }
  }
}
</script>

<style type="text/css">
.row{
  margin-top: 20px;
}
</style>