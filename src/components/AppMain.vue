<script>

import AppCard from './AppCard.vue';

// import data from '../assets/db.json'
import { store } from '../store.js'

    export default{
        data(){
            return{
                store
            }
        },
        components: {
            AppCard,
          
        }
    }
</script>

<template>
    <main class="page-main">
        <div class="container">
            <div class="page-content">
                <div class="row">
                    <ul>
                        <li v-for="product in store.products" :key="product.id" class="col-4">
                          <AppCard :singleProduct="product"/>
                            <!-- <div class="card">
                                <div class="card-header">
                                    <img :src="product.imgBase" alt="">
                                    <div class="overlay">
                                        <a href="#"><img :src="product.imgOver" alt=""></a>
                                    </div>
                                </div>
                                <div class="card-body">
                                    <span class="save" @click="product.saved = !product.saved":class="product.saved === true ? 'saved': ''">&hearts;</span>
                                    <div class="img-badge">
                                        <span :class="product.discount !== ''? 'red': ''" class="badge">{{ product.discount }}</span>
                                        <span :class="product.ecoGreen !== ''? 'green': ''" class="badge">{{ product.ecoGreen }}</span>
                                    </div>
                                    <p class="clothing-brand">{{ product.brand }}</p>
                                    <p class="clothing-type">{{ product.name }}</p>
                                    <span class="price">{{ product.price }}&euro;</span>
                                    <span class="price-discount">{{ product.priceDiscount }}&euro;</span>
                                </div>
                            </div> -->

                        </li> 
                    </ul>
    
                </div>

            </div>
        </div>
        
    </main>
</template>

<style lang="scss" scoped>

@use '../style/partials/variables' as*;
@use '../style/partials/mixins' as*;

ul{
    display: flex;
    flex-wrap: wrap;
}

// .card .clothing-brand, .price-discount{
//     color: $color-grey;
// }
// .card .price-discount{
//     text-decoration: line-through;
// }

// .badge{
//     @include badge-mixin;
// }
// .card{

//     &:hover .overlay{
//     opacity: 1;
//     }
//     position: relative;
//     .red{
//     background-color: $color-red;
//     }
//     .green{
//     background-color: $color-green; 
//     }
//     .price{
//     color: $color-red;
//     }

// } 
// .saved{
//     color: $color-red
// }

// .save{
//   @include save-mixin;
  
// }

// .overlay{
//     @include overlay-mixin;
// }

// .img-badge{
//    @include img-badge-mixin;
// }


</style>