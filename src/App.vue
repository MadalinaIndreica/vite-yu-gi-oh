<script>

import axios from "axios";
import { store } from "./store.js";
import AppHeader from "./components/AppHeader.vue";
import AppCardList from "./components/AppCardList.vue";
export default {
  data() {
    return {
      
      store,
    };
  },
  created() {
    
    axios.get(this.store.apiUrl).then((resp) => {
      
      this.store.cards = resp.data.data;
      
    });
  },
  components: { AppHeader, AppCardList },
};


</script>

<template>
   <AppHeader />
   <AppCardList />
</template>

<style lang="scss">
@use "./style/general.scss";

</style>
