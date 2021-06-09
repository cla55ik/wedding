<template>
    <div class="introduction">
        <div>
            <h2>Привет</h2>
        </div>
        <div>
            <p>Надеемся, что ты помнишь про&nbsp;нашу свадьбу и&nbsp;готов к&nbsp;веселью и&nbsp;позитиву</p>
        </div>
        <div>
            <p>А чтобы тебе было комфортно мы подготовили небольшой путеводитель по&nbsp;этому мероприятию:</p>
        </div>
    </div>
    
</template>

<script>
export default {
    
}
</script>
<style scoped>
    h2{
        font-size:32px; 
        text-align: center;   
    }
    p{
        font-size: 24px;
        line-height: 1.5em;
    }
    .introduction{
        margin: 60px auto;
        padding: 0px 15px;
    }


    @media screen and (min-width: 475px){
        h2{
            margin-top: 103px;
            font-size: 46px;
        }

        p{
            font-size: 28px;
        }
    }
</style>