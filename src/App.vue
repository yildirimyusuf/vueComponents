<template>
  <div class="info-header">
    <DataDisplayer
        :Header="Header"
        :datas="datas"
    />
  </div>
</template>

<script>
import DataDisplayer from './components/DataDisplayer.vue'

export default {
  name: 'app',
  components: {
    DataDisplayer
  },
  data() {
    return {
      Header: "Buraya Header Gelecek",
      datas:[
        {
          key: 'Ek Hesap Limiti',value:' 500 TL'
        },
        {
          key: 'Ek Hesap Toplam Borç',value:' 200 TL'
        },
        {
          key: 'Ek Hesap Faiz Borcu',value:' 1000 TL'
        },
        {
          key: 'Ek Hesap Kullanılabilir Limiti',value:' 1000 TL'
        }
      ]
    }
  }
}
</script>

