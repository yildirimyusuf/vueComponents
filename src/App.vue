<template>
  <div class="info-header">
    <Info
        :Header="Header"
        :Text="Text"
        :Style="Style"
        :Icon="Icon"
        :Border="Border"
        :FontType="FontType"
    />
  </div>
</template>

<script>
import Info from './components/Info.vue';
import Data from './components/Data.vue';

export default {
  name: 'app',
  components: {
    Info,
    Data
  },
  data() {
    return {
      Header: "",
      Text: "Info Text",
      Style: "green-info",
      Icon: "",
      Border: true
    }
  }
}
</script>

