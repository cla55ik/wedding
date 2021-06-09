<template>
    <div class="plan-container">
        <div>
            <h2>- Что будет?</h2>
        </div>
        <div class="plan-list">
             <div class="plan-item d-flex align-items-center">
                <img src="~@/assets/icon/emoticons.svg" alt="">
                <span>Приятные люди</span>
            </div>
             <div class="plan-item d-flex align-items-center">
                <img src="~@/assets/icon/smiley.svg" alt="">
                <span>Хорошее настроение</span>
            </div>
            <div class="plan-item d-flex align-items-center">
                <img src="~@/assets/icon/yes.svg" alt="">
                <span>Позитивная атмосфера</span>
            </div>
            <div class="plan-item d-flex align-items-center">
                <img src="~@/assets/icon/glass.svg" alt="">
                <span>Легкий фуршет</span>
            </div>
             <div class="plan-item d-flex align-items-center">
                <img src="~@/assets/icon/eat.svg" alt="">
                <span>Плотный банкет</span>
            </div>
             <div class="plan-item d-flex align-items-center">
                <img src="~@/assets/icon/cocktail.svg" alt="">
                <span>Ипровизированный бар</span>
            </div>
             <div class="plan-item d-flex align-items-center">
                <img src="~@/assets/icon/dancer.svg" alt="">
                <span>Безудержные танцы</span>
            </div>
             <div class="plan-item d-flex align-items-center">
                <img src="~@/assets/icon/trophy.svg" alt="">
                <span>Веселые конкурсы</span>
            </div>
             <div class="plan-item d-flex align-items-center">
                <img src="~@/assets/icon/camera.svg" alt="">
                <span>Яркие фотографии</span>
            </div>
            

        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>

    .plan-container{
        padding: 25px;
    }

    .plan-list{
        margin-left: 15px;
    }

    .plan-item{
        margin: 15px 0px;
    }   

    .plan-item img{
        width: 35px;
        height: auto;
        object-fit: contain;
        margin-right: 10px;
    } 

    .plan-item span{
        font-size: 24px;
    }


    @media screen and (min-width:475px) {

        h2{
            text-align: center;
        }
         .plan-list{
            display: flex;
            justify-content:center;
            flex-wrap: wrap;
            margin: auto 0px;
        }

        .plan-item{
            display:flex;
            justify-content: center;
            width: 30%;
        }
    }
</style>