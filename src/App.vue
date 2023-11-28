<script>

import axios from "axios";
import { store } from "./store.js";
import AppHeader from "./components/AppHeader.vue";
import AppCardList from "./components/AppCardList.vue";
import AppButton from "./components/AppButton.vue";

export default {
  data() {
    return {
      
      store,
    };
  },
  created() {
    axios
      .get(this.store.apiUrl, {
        params: {
          num: 20,
          offset: 0
        },
      })
      .then((resp) => {
        //console.log(resp);
        this.store.cards = resp.data.data;
      
      })
  },
  components: { AppHeader, AppCardList, AppButton},
  methods: {
    handleSelect() {
        axios.get(this.store.apiArcUrl, {
          params: {
            archetype: this.store.selectedOption,
            num: 20,
            offset: 0
          }
        }).then((resp) => {
          this.store.cards = resp.data.data;
        })
      }
    }
};


</script>

<template>
   <AppHeader />
   <AppButton @cardsView="handleSelect"/>
   <AppCardList />
   
</template>

<style lang="scss">
@use "./style/general.scss";

</style>
