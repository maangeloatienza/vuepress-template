<template>
    <div class="container">
        <div class="row">
            <h1>{{product.name}}</h1>
           
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