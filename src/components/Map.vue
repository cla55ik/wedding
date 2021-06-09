<template>
    <div class="map-wrapper">
        <div class="text">
            <h2>- Как проехать</h2>
            <p> Новый банкетный зал Val De Bo, расположен в&nbsp;100м от&nbsp;основного комплекса Адмирал</p>
        </div>
        <div class="map-inner">
            <div class="ya-map" @load="getMapContainer">
                <iframe src="https://yandex.ru/map-widget/v1/?um=constructor%3A144a77e54702f5eb17ee69aecae941469e156a928c8a246b8fd1858312349531&amp;source=constructor" width="100%" height="400px" frameborder="0" ></iframe>
            </div>
        </div>
    </div>
</template>

<script>
export default {

    
}
</script>

<style scoped>

.green {
    background-color: teal;
}

iframe{
    border-radius: 0px 30px 30px 0px !important;
    }
h2{
    text-align: left;
    font-size: 28px;
    margin-bottom: 5px;
}

.text{

    margin: 0px 25px;
    
}

.text p{
    text-align: left;
    font-size: 20px;
    line-height: 1.3em;
    margin-top: 0;
}


.map-inner{
    margin: 30px 25px 0px 0px;
    background-color: #FDE9F3;
    border-radius: 0px 50px 50px 0px;
    padding: 25px 25px 25px 0px;
    -webkit-box-shadow: 2px -5px 4px 0px rgba(92, 50, 50, 0.57);
        -moz-box-shadow:    2px -5px 4px 0px rgba(92, 50, 50, 0.57);
        box-shadow:         2px -5px 4px 0px rgba(92, 50, 50, 0.57);
}

.ya-map{
    border: 5px solid white;
    border-radius: 0px 30px 30px 0px;
}

@media screen and (min-width: 475px){

    h2{
        font-size: 42px;

    }

    .text p{
        font-size: 24px;
    }

    .map-inner{
        margin-top: 50px;
        border-radius: 50px;
        padding: 40px;
       
        
    }

    iframe{
        border-radius: 30px !important;
    }

    .ya-map{
    
    border-radius: 30px;
}
    .map-wrapper{
        margin: 0px 125px;
    }

}
</style>