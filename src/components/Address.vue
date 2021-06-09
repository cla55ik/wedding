<template>
    <div class="address d-flex flex-wrap justify-around">
        <div class="where">
            <h2> - Где и во сколько</h2>
        </div>
        <div>
            <div class="item d-flex align-items-center justify-around">
                <div class="col-2 d-flex align-items-center">
                    <img src="@/assets/icon/geo.svg" alt="">
                </div>
                <div class="col-10 d-flex flex-wrap align-items-center">
                    <div class="title">Клубный ресторан АДМИРАЛ</div>
                    <div class="subtitle">Московский пр., 146</div>
                </div>
            </div>
            <div class="item  d-flex align-items-center">
                <div class="col-2 d-flex flex-wrap align-items-center justify-end">
                    <img src="@/assets/icon/clock.svg" alt="">
                </div>
                <div class="col-10 d-flex  align-items-center justify-end">
                    <div class="title">Сбор гостей в 16:30</div>
                    
                </div>
            </div>
        </div>
    </div>
</template>

<script>


export default ({
   
})
</script>

<style scoped>

h2{
    text-align: left;
    font-size: 28px;
}

.address{
    margin: 0px 25px;
    padding: 40px 0px 120px 0px;
    
}

.address .title{
    text-align: right;
    font-weight: normal;
    font-size: 28px;
    line-height: 29px;
    width: 100%;
}

.address .subtitle{
    text-align: right;
    font-weight: normal;
    font-size: 20px;
    line-height: 26px;
    width: 100%;
}

.item{
    margin: 20px 0px;
}

.address img{
    width: 40px;
}

@media screen and (min-width:475px) {
  
    h2{
            font-size: 42px;
            
        }

    .where{
        margin: auto 0px;
    }
    
}

</style>