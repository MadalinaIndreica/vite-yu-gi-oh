<script>
export default {
    props: {
    card: Object,
  },

}


</script>

<template>

    <div >
    <img :src="card.card_images[0].image_url" alt="" />
    <h4>{{ card.name }}</h4>

  </div>

</template>

<style lang="scss" scoped>
div{
    background-color: rgb(212 143 56);
   
   
}
img {
    max-width: 100%;
    

        
    
}

</style>