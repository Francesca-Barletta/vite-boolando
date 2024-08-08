<script>
export default {
    props: {
        open: {
            type: Boolean,
            default:false
        },
        item : Object,
    },
    methods: {
       
    },

}

</script>

<template>
    <div v-if="open"  @click="$emit('exit')" class="modal-wrapper">
        <div class="modal">
            <img id="modal-img" :src="item.frontImage" alt="">
            <p>{{item.brand}}</p>
            <p>{{item.name}}</p>
            <p>{{item.price}}</p>
            <div class="action">
                <button data-confirm="esci" @click="$emit('exit')">Esci</button>
            </div>
        </div>
    </div>

</template>

<style lang="scss">
.modal-wrapper{
    position:fixed;
    z-index: 999;
    top:0;
    bottom:0;
    left:0;
    right:0;
    background: rgba(black, 0.8);
    display:flex;
    align-items:center;
    justify-content:center;
    padding:20px;
}
.modal{
    display:flex;
    flex-direction:column;
    justify-content: center;
    align-items: center;
    background: white;
    padding:16px;
    border-radius:20px;
    .action{
        display:flex;
        gap:12px;
        justify-content: center;
        margin-top: 12px;
        button{
            border: none;
            line-height:24px;
            padding:0 12px;
            border-radius:900px;
            cursor: pointer;
           &[data-confirm="esci"] {

               background: red;
               color:white;
           }
           &:hover{
            background: rgb(177, 15, 15);
           }
        }
    }
    #modal-img{
        width:60%;
    }
}
</style>