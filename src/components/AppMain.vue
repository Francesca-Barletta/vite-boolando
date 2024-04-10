<script>
    export default{
        data(){
            return{
              products:[
                {
                    imgBase: '/1.webp',
                    imgOver: '/1b.webp',
                    discount: '-50%',
                    ecoGreen: 'Sostenibilità',
                    brand:'Levis',
                    name: 'RELAXED FIT TEE UNISEX',
                    price: 14.99,
                    priceDiscount: 29.99
                },
                {
                    imgBase: '/2.webp',
                    imgOver: '/2b.webp',
                    discount: '-30%',
                    ecoGreen: '',
                    brand:'Guess',
                    name: 'ROSES TEE',
                    price: 20.99,
                    priceDiscount: 29.99
                },
                {
                    imgBase: '/3.webp',
                    imgOver: '/3b.webp',
                    discount: '-30%',
                    ecoGreen: '',
                    brand:'Come Zucchero Filato',
                    name: 'VOGLIA DI COLORI PASTELLO',
                    price: 129.99,
                    priceDiscount: 184.99
                },
                {
                    imgBase: '/4.webp',
                    imgOver: '/4b.webp',
                    discount: '-50%',
                    ecoGreen: 'Sostenibilità',
                    brand:'Levis',
                    name: 'TEE UNISEX',
                    price: 14.99,
                    priceDiscount: 29.99
                },
                {
                    imgBase: '/5.webp',
                    imgOver: '/5b.webp',
                    discount: '',
                    ecoGreen: '',
                    brand:'Maya Deluxe',
                    name: 'STRIPE BODICE',
                    price: 99.99,
                    priceDiscount: ''
                },
                {
                    imgBase: '/6.webp',
                    imgOver: '/6b.webp',
                    discount: '',
                    ecoGreen: 'Sostenibilità',
                    brand:'Esprit',
                    name: 'MAGLIONE - BLACK',
                    price: 29.99,
                    priceDiscount: ''
                }
              ]  
            }
        }
    }
</script>

<template>
    <main class="page-main">
        <div class="container">
            <div class="page-content">
                <div class="row">
                    <ul>
                        <li v-for="product in products" class="col-4">

                            <div class="card">
                                <div class="card-header">
                                    <img :src="product.imgBase" alt="">
                                    <div class="overlay">
                                        <a href="#"><img :src="product.imgOver" alt=""></a>
                                    </div>
                                </div>
                                <div class="card-body">
                                    <span class="save">&hearts;</span>
                                    <div class="img-badge">
                                        <span :class="product.discount !== ''? 'red': ''" class="badge">{{ product.discount }}</span>
                                        <span :class="product.ecoGreen !== ''? 'green': ''" class="badge">{{ product.ecoGreen }}</span>
                                    </div>
                                    <p class="clothing-brand">{{ product.brand }}</p>
                                    <p class="clothing-type">{{ product.name }}</p>
                                    <span class="price">{{ product.price }}&euro;</span>
                                    <span class="price-discount">{{ product.priceDiscount }}&euro;</span>
                                </div>
                            </div>

                        </li>
                    </ul>
    
                </div>

            </div>
        </div>
    </main>
</template>

<style lang="scss">

@use '../style/partials/variables' as*;
@use '../style/partials/mixins' as*;

ul{
    display: flex;
    flex-wrap: wrap;
}

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