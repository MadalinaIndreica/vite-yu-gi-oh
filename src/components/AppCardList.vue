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
    <div class="container">

        <div class="row">
            <div class="col" v-for="card in store.cards" :key="card.id">
                <AppCard :card="card" />
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped></style>