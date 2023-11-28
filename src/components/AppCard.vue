<script>
export default {
    props: {
        card: Object,
    },

}


</script>

<template>
    <div  class="card h-100 text-center">
        <img :src="card.card_images[0].image_url_small" alt="Card.name" />
        <div class="card-body">
            <h5 class="card-text"> {{ card.name }}</h5>
            <p> {{ card.archetype ? card.archetype : "nessun archetype" }}</p>
        </div>
       
    </div>
</template>

<style lang="scss" scoped>
div {
    background-color: rgb(255, 160, 43);
    .card-text{
        color: white;
    }

}

img {
    max-width: 100%;
}
</style>