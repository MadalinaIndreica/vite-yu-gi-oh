<script>
export default {
    props: {
    card: Object,
  },

}


</script>

<template>

     <div>
    <img :src="card.card_images[0].image_url" alt="" />
    <h3>{{ card.name }}</h3>

  </div>

</template>

<style lang="scss" scoped>

</style>