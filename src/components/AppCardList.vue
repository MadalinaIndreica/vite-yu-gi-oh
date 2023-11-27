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

        <div class="row ">
            <div class="col-3 align-items-stretch" v-for="card in store.cards" :key="card.id">
                <AppCard :card="card" />
            </div>
        </div>
    </div>
    </div>
</template>

<style lang="scss" scoped>
.section{
    background-color:rgb(212 143 56);
    padding:4rem;

}
    .container {
        background-color: white;
       
    }
</style>