<script>

</script>

<template>
 <main class="page-main">
        <div class="container">
            <div class="page-content">
                <div class="row">
                    <div class="col-4">
                        <div class="card">
                            <div class="card-header">
                                <img src="/1.webp" alt="uomo con maglietta Levi's">
                                <div class="overlay">
                                    <a href="#"><img src="/1b.webp" alt=""></a>
                                </div>
                            </div>
                            <div class="card-body">
                                <span class="save">&hearts;</span>
                                <div class="img-badge">
                                    <span class="red">-50%</span>
                                    <span class="green">Sostenibilità</span>
                                </div>
                                <p class="clothing-brand">Levi's</p>
                                <p class="clothing-type">RELAXED FIT TEE UNISEX</p>
                                <span class="price">14,99&euro;</span>
                                <span class="price-discount">29,99&euro;</span>
                            </div>
                        </div>
                    </div>

                    <div class="col-4">
                        <div class="card">
                            <div class="card-header">
                                <img src="/2.webp" alt="donna con t-shirt Guess">
                                <div class="overlay">
                                    <a href=""><img src="/2b.webp" alt=""></a>
                                </div>
                            </div>
                            <div class="card-body">
                                <span class="save">&hearts;</span>
                                <div class="img-badge">
                                    <span class="red">-30%</span>
                                </div>
                                <p class="clothing-brand">Guess</p>
                                <p class="clothing-type">ROSES TEE</p>
                                <span class="price">20,99&euro;</span>
                                <span class="price-discount">29,99&euro;</span>
                            </div>
                        </div>
                    </div>

                    <div class="col-4">  
                        <div class="card">
                            <div class="card-header">
                                <img src="/3.webp" alt="donna con completo verde chiaro">
                                <div class="overlay">
                                    <a href=""><img src="/3b.webp" alt=""></a>
                                </div>
                            </div>
                            <div class="card-body">
                                <span class="save">&hearts;</span>
                                <div class="img-badge">
                                    <span class="red">-30%</span>
                                </div>
                                <p class="clothing-brand">Come Zucchero Filato</p>
                                <p class="clothing-type">VOGLIA DI COLORI PASTELLO</p>
                                <span class="price">129,99&euro;</span>
                                <span class="price-discount">184,99&euro;</span>
                            </div>
                        </div>
                    </div>

                    <div class="col-4">
                        <div class="card">
                            <div class="card-header">
                                <img src="/4.webp" alt="uomo con t-shirt Levi's">
                                <div class="overlay">
                                    <a href=""><img src="/4b.webp" alt=""></a>
                                </div>
                            </div>
                            <div class="card-body">
                                    <span class="save">&hearts;</span>
                                    <div class="img-badge">
                                        <span class="red">-50%</span>
                                        <span class="green">Sostenibilità</span>
                                    </div>
                                <p class="clothing-brand">Levi's</p>
                                <p class="clothing-type">TEE UNISEX</p>
                                <span class="price">14,99&euro;</span>
                                <span class="price-discount">29,99&euro;</span>
                            </div>
                        </div>
                    </div>

                    <div class="col-4">
                        <div class="card">
                            <div class="card-header">
                                <img src="/5.webp" alt="donna con abito Maya Deluxe">
                                <div class="overlay">
                                    <a href=""><img src="/5b.webp" alt=""></a>
                                </div>
                            </div>
                            <div class="card-body">
                                <span class="save">&hearts;</span>
                                <p class="clothing-brand">Maya Deluxe</p>
                                <p class="clothing-type">STRIPE BODICE</p>
                                <span class="price">99,99&euro;</span>
                            </div>

                        </div>
                    </div>

                    <div class="col-4">
                        <div class="card">
                            <div class="card-header">
                                <img src="/6.webp" alt="Donna con maglione Esprit">
                                <div class="overlay">
                                    <a href=""><img src="/6b.webp" alt=""></a>
                                </div>
                            </div>
                            <div class="card-body">
                                <span class="save">&hearts;</span>
                                <div class="img-badge">
                                    <span class="green">Sostenibilità</span>
                                </div>
                                <p class="clothing-brand">Esprit</p>
                                <p class="clothing-type">MAGLIONE - BLACK</p>
                                <span class="price">29,99&euro;</span>
                            </div>
                            
                        </div>
                    </div>
                    
                   
                </div>

            </div>
        </div>
    </main>
</template>

<style lang="scss">

.card .clothing-brand, .price-discount{
    color: grey;
}
.card .price-discount{
    text-decoration: line-through;
}

.card .red, .green{
    
    color: white;
    font-size: 12px;
    padding: 4px;
}
.card .red{
    background-color: red;
}
.card .green{
    background-color: green;
    color: white;
}
.card .price{
    color: red;
}

.card .save{
    background-color: white;
    padding: 5px 8px;
    font-size: 20px;
    line-height: 20px;
}

.card .overlay{
    position: absolute;
    top: 0;
    left: 0;
    opacity: 0;
    padding: 10px;
}
.card:hover .overlay{
    opacity: 1;
}

</style>