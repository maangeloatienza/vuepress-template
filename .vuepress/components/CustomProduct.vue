<template>
    <div class="container">
        <div class="mt-3 mb-3">
            <div v-if="typeof product.image == Object" class="text-center">
                <img 
                    :src="`${product.image.link}`"
                    :alt="`${product.image.meta}`"
                    class="img-fluid img-thumbnail">
                <p class=""> <b>Figure 1:</b> {{product.image.caption}}</p>
            </div>

            <div v-if="typeof product.image == Array" class="text-center">
                <div v-for="image in product.image">
                    <div class="card">
                        <img 
                            :src="`${image.link}`"
                            :alt="`${image.meta}`"
                            class="img-fluid img-thumbnail">
                        <p class=""> <b>Figure 1:</b> {{product.caption}}</p>
                    </div>
                    
                </div>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    props : {
        product : {type: Object}
    },
    data (){
        return {

        }
    }
}
</script>

<style scoped>

</style>