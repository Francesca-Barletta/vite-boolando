<script>
export default{
    data(){
        return{
            productIndex: 0,
            badgeIndex: 0
        }
    },
    props:{
        singleProduct: Object,
        badges: Array
    },
    mounted(){
        console.log(this.singleProduct.badges[1])
    }
}
</script>

<template>
    
        <div class="card">
            <div class="card-header">
                <img :src="singleProduct.frontImage" alt="uomo con maglietta Levi's">
                <div class="overlay">
                    <a href="#"><img :src="singleProduct.backImage" alt=""></a>
                </div>
            </div>
            <div class="card-body">
                <span class="save">&hearts;</span>
                <ul v-for="(badgeObject, i) in singleProduct.badges" :key="i" class="img-badge">
                    <li v-if="badgeObject.type == 'discount'" class="badge red">{{ badgeObject.value }}</li>
                    <li v-if="badgeObject.type == 'tag'" class="badge green">{{ badgeObject.value }}</li>
                </ul>
                <p class="clothing-brand">{{singleProduct.brand}}</p>
                <p class="clothing-type">{{ singleProduct.name }}</p>
                <span class="price">{{singleProduct.price}}&euro;</span>
                <span class="price-discount">29,99&euro;</span>
            </div>
        </div>
 


</template>

<style lang="scss">

@use '../style/partials/variables' as*;
@use '../style/partials/mixins' as*;


.card .clothing-brand, .price-discount{
    color: $color-grey;
}
.card .price-discount{
    text-decoration: line-through;
}

.badge{
    @include badge-mixin;
}
.card {
    position: relative;

    &:hover .overlay{
        opacity: 1;
    }
    .red{
        background-color: $color-red;
    }
    .green{
        background-color: $color-green; 
    }
    .price{
        color: $color-red;
    }

} 
.saved{
    color: $color-red
}

.save{
  @include save-mixin;
  
}

.overlay{
    @include overlay-mixin;
}

.img-badge {
    position: absolute;
    left: 10px;
    bottom: 100px;
}

</style>