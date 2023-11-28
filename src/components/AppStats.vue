<script>
import { store } from "../store";
export default {
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <div class="container">
    <p class="text-end">Totale {{ store.cards.length }} card</p>
  </div>
</template>