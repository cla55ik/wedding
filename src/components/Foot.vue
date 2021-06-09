<template>
<div class="foot-wrapper d-flex flex-wrap justify-center">
    <h2>Ждем с нетерпением!</h2>
    <img src="~@/assets/img/cats.jpg" alt="">
</div>
    
</template>
<script>
export default {
    
}
</script>

<style scoped>
   .foot-wrapper h2{
        font-size: 32px;
        text-align: center;
    }
   .foot-wrapper img{
        margin-top: 30px;
        width: 70%;
        height: auto;
        object-fit: contain;
    }

    .foot-wrapper{
        margin-bottom: 30px;
    }

    @media screen and (min-width:475px){
        .foot-wrapper h2{
            font-size: 52px;
        }

        .foot-wrapper{
            justify-content: space-around;
            align-items: center;
        }

        .foot-wrapper img{
            width: 25%;
        }

       
    }
</style>