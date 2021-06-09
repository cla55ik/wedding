<template>
<div class="header-wrapper">
    <h1>СВАДЬБА</h1>
    <div class="title-names">Иван и Мария</div>
</div>
<div class="date-wedding">
    <span>11 июня 2021</span>
    
</div>
    
</template>
<script>


export default({
   
})
</script>

<style scoped>


    .header-wrapper{
        /*background-color: #FDE9F3;*/
        background-image: url('~@/assets/img/bg-2.jpg');
        background-repeat: no-repeat;
        background-position: center right;
        background-size: cover;
        border-radius: 0px 0px 50px 50px;
        padding-top:35px;
        padding-bottom: 60px;

        -webkit-box-shadow: 0px 5px 4px 0px rgba(92, 50, 50, 0.57);
        -moz-box-shadow:    0px 5px 4px 0px rgba(92, 50, 50, 0.57);
        box-shadow:         0px 5px 4px 0px rgba(92, 50, 50, 0.57);
    }

    h1{
        font-family: 'Yanone';
        font-style: normal;
        font-weight: normal;
        font-size: 36px;
        line-height: 43px;
    }



    .date-wedding span{
    font-family: 'Yanone';
    font-style: normal;
    font-weight: normal;
    font-size: 28px;
    line-height: 33px;

    color: #FFFFFF;
    background-color: #501B32;
    padding: 10px 60px;
    border-radius:20px;

    -webkit-box-shadow: 0px 0px 11px 0px rgba(92, 50, 50, 0.32);
    -moz-box-shadow:    0px 0px 11px 0px rgba(92, 50, 50, 0.32);
    box-shadow:         0px 0px 11px 0px rgba(92, 50, 50, 0.32);
    
    }

     .date-wedding{
         margin-top: -20px;
     }

    @media screen and (min-width:475px) {
    .header-wrapper {
        padding-top:35px;
        padding-bottom: 60px;
    }
    }

</style>