<script>
import AppModal from './AppModal.vue';
export default{
    components: {
        AppModal
    },
    props:{
        singleProduct: Object,
        badges: Array
    },
    data() {
        return {
            isOpen :false,
        }

    },
    methods: {
        openModal() {
            this.isOpen = true;
        }
    },
    mounted(){
        console.log(this.singleProduct.badges[1])
    }
}
</script>

<template>
    
        <div class="card" @click="openModal">
            <div class="card-header">
                <img :src="singleProduct.frontImage" alt="uomo con maglietta Levi's">
                <div class="overlay">
                    <a href="#"><img :src="singleProduct.backImage" alt=""></a>
                </div>
            </div>
            <div class="card-body">
                <span @click="singleProduct.isInFavorites = !singleProduct.isInFavorites" 
                :class="singleProduct.isInFavorites == false ? 'save':'saved'">&hearts;</span>
                <ul class="img-badge">
                    <li v-for="(badgeObject, i) in singleProduct.badges" :key="i" 
                       :class="badgeObject.type" class="badge">{{ badgeObject.value }} "</li>
                    
                </ul>
                <p class="clothing-brand">{{singleProduct.brand}}</p>
                <p class="clothing-type">{{ singleProduct.name }}</p>
                <span class="price">{{singleProduct.price}}&euro;</span>
                <span class="price-discount">29,99&euro;</span>
            </div>
        </div>
 
  <AppModal :open="isOpen" :item="singleProduct" @exit="isOpen = false"/>

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
    .discount{
        background-color: $color-red;
        color:white;
        order: -1;
    }
    .tag{
        background-color: $color-green; 
        color:white;
    }
    .price{
        color: $color-red;
    }

} 
.saved{
    color: $color-red;
    @include save-mixin;
  
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
    display:flex;

}

</style>