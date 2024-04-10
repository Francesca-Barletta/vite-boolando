<script>

</script>

<template>
    <footer class="page-footer">
        <div class="container container-ft">
            <div class="row row-footer">
                <div class="col-info">
                    <h3><a href="#">Boolando SRL</a></h3>

                    <ul class="footer-info">
                        <li><a href="">informazioni sulla privacy</a></li>
                       
                        <li><a href="">informazioni legali</a></li>
                       
                        <li><a href="">diritto di recesso</a></li>
                      
                    </ul>

                </div>
                <div class="col-social">
                    <h4>Trovaci anche su</h4>

                    <ul class="footer-social">
                        <li><a href=""><img src="/icons8-facebook-24.png" alt=""></a></li>
                        <li><a href=""><img src="/icons8-instagram-24.png" alt=""></a></li>
                        <li><a href=""><img src="/icons8-riproduci-youtube-24.png" alt=""></a></li>
                        <li><a href=""><img src="/icons8-twitter-24.png" alt=""></a></li>
                        <li><a href=""><img src="/icons8-pinterest-24.png" alt=""></a></li>
                    </ul>

                </div>
            </div>
        </div>
    </footer>

</template>

<style lang="scss">
.page-footer{
    background-color: black;
    color: white;
}
.row-footer{
    justify-content: space-between;
}
h4, li{
    display: inline-block;
}


.footer-info, .footer-social{
    display: flex;
    flex-direction: row;
    gap: 5px;
    font-size: 12px;
}
.row-footer{
    position: relative;
}
.col-social{
    position: absolute;
    right: 0px;
}
</style>