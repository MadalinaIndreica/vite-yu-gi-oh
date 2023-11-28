<script>
import { store } from "../store";
import AppCard from "./AppCard.vue";
export default {
    data() {
        return {
            store,
        };
    },
    components: { AppCard },

};

</script>

<template>
    <div class="section">
    <div class="container">

        <div class="row row-cols-5 g-4 mt-5">
            <div class="align-items-stretch" v-for="card in store.cards" :key="card.id">
                <AppCard :card="card" />
            </div>
        </div>
    </div>
    </div>
</template>

<style lang="scss" scoped>
.section{
    background-color:rgb(255, 160, 43);
    padding:4rem;

}
    .container {
        background-color: white;
       
    }
</style>