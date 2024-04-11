<script>

import AppCard from './AppCard.vue';

    export default{
        data(){
            return{
                "products": [
                    {
                        "id": 1,
                        "frontImage": "1.webp",
                        "backImage": "1b.webp",
                        "brand": "Levi's",
                        "name": "Relaxed Fit",
                        "price": 29.99,
                        "isInFavorites": true,
                        "badges": [
                            {
                                "type": "tag",
                                "value": "Sostenibilità"
                            },
                            {
                                "type": "discount",
                                "value": "-50%"
                            }
                        ]
                    },
                    {
                        "id": 2,
                        "frontImage": "2.webp",
                        "backImage": "2b.webp",
                        "brand": "Guess",
                        "name": "Roses Tee",
                        "price": 20.99,
                        "isInFavorites": true,
                        "badges": [
                            {
                                "type": "discount",
                                "value": "-30%"
                            }
                        ]
                    },
                    {
                        "id": 3,
                        "frontImage": "3.webp",
                        "backImage": "3b.webp",
                        "brand": "Come Zucchero Filato",
                        "name": "Voglia di colori pastello",
                        "price": 129.99,
                        "isInFavorites": false,
                        "badges": [
                            {
                                "type": "discount",
                                "value": "-30%"
                            }
                        ]
                    },
                    {
                        "id": 4,
                        "frontImage": "4.webp",
                        "backImage": "4b.webp",
                        "brand": "Levi's",
                        "name": "Tee Unisex",
                        "price": 14.99,
                        "isInFavorites": false,
                        "badges": [
                            {
                                "type": "tag",
                                "value": "Sostenibilità"
                            },
                            {
                                "type": "discount",
                                "value": "-50%"
                            }
                        ]
                    },
                    {
                        "id": 5,
                        "frontImage": "5.webp",
                        "backImage": "5b.webp",
                        "brand": "Maya Deluxe",
                        "name": "Stripe Bodice",
                        "price": 99.99,
                        "isInFavorites": true,
                        "badges": [
                            {
                                "type": "tag",
                                "value": "Sostenibilità"
                            },
                            {
                                "type": "discount",
                                "value": "-50%"
                            }
                        ]
                    },
                    {
                        "id": 6,
                        "frontImage": "6.webp",
                        "backImage": "6b.webp",
                        "brand": "Esprit",
                        "name": "Maglione - Black",
                        "price": 29.99,
                        "isInFavorites": true,
                        "badges": [
                            {
                                "type": "tag",
                                "value": "Sostenibilità"
                            }
                        ]
                    }
                ]
            }
        },
        components: {
            AppCard
        }
    }
</script>

<template>
    <main class="page-main">
        <div class="container">
            <div class="page-content">
                <div class="row">
                    <ul>
                        <li v-for="(product,i) in products" :key="i" class="col-4">
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