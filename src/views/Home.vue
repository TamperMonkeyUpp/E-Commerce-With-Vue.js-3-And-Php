<template>
    <div class="container w-full h-auto items-center justify-center mx-auto mt-10">
        <Carousel/>
    </div>
    <div class="container mx-auto justify-center items-center">
        <Product/>
        <ProductCardPopup/>
    </div>
</template>

<script>
import Carousel from '../components/Carousel.vue'
import Product from '../components/Product.vue'
export default {
    components:{
        Carousel,
        Product,
    }
}
</script>

<style>

</style>
