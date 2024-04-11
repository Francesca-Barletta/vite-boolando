<script>
export default{
    props:['singleProduct']
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
                <div class="img-badge">
                    <span class="red">-50%</span>
                    <span class="green">Sostenibilità</span>
                </div>
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
.card{

    &:hover .overlay{
    opacity: 1;
    }
    position: relative;
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

.img-badge{
   @include img-badge-mixin;
}

</style>