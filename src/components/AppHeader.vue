<script>
export default {
    data() {
        return {
            headerType: [
                'Donna',
                'Uomo',
                'Bambino'
              
            ],
            headerMenu:[
                'login',
                'Save-list',
                'Cart'
            ]
        }
    }
}
</script>

<template>
    <header class="page-header">
        <div class="container container-hd">
            <div class="row row-header">

                <div>
                    <ul class="choose-type">
                        <li v-for="gen in headerType"><a href="#">{{ gen }}</a></li>

                    </ul>
                </div>

                <div class="header-logo">
                    <img src="/boolean-logo.png" alt="logo-Boolean">
                </div>

                <div>
                    <ul class="header-menu">
                        <li v-for="icon in headerMenu"><a href="">{{ icon }}</a></li>
                    </ul>
                </div>

            </div>
        </div>
    </header>

</template>

<style lang="scss">
.page-header {
    background-color: rgb(255, 119, 0);
    position: fixed;
    width: 100%;
    z-index: 999;
}

.page-main {
    padding-top: 100px;
}

.page-header .container {
    color: white;
}

.page-header .header-logo {
    width: 200px;
}
</style>