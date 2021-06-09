<template>
    <div class="table-container">
        <div class="table-container-title">
            <h2>- Схема рассадки</h2>
        </div>
    
        <div class="tables-wrapper">
            
            <div class="guest-change d-flex justify-center align-items-center" v-show="visTable">
                <div>Поиск по Имени гостя: </div>
                <select v-model="currentGuest" @change="searchTable">
                    <option v-for="(guest, index) in guests" v-bind:key="index">{{guest.name}}</option>
                </select>
            </div>
            
                <div class="current-table" v-show="currentTable">
                    
                        <span>Ваш стол {{currentTable}}</span> 
                    
                </div>
           
           
            <div v-show="visTable" class="tabs-content table">
                <div>
                    <div class="table-title">Стол молодых</div>
                    <img src="@/assets/icon/table-main.svg" alt="">
                </div>
                <div class="d-flex justify-around table-row">
                    <div>
                        <div class="table-title parent">Родные Марии</div>
                        <img src="@/assets/icon/table-bw.svg" alt="" v-show="currentTable != 5">
                        <img src="@/assets/icon/table-color.svg" alt="" v-show="currentTable == 5">
                    </div>
                    <div>
                        <div class="table-title parent">Родные Ивана</div>
                        <img src="@/assets/icon/table-bw.svg" alt="" v-show="currentTable != 6">
                        <img src="@/assets/icon/table-color.svg" alt="" v-show="currentTable == 6">
                    </div>
                </div>
                <div class="d-flex justify-around table-row">
                    <div>
                        <div class="table-title" v-show="currentTable != 1">Стол 1</div>
                        <div class="table-title-check" v-show="currentTable == 1"> Ваш Стол 1</div>
                        <img src="@/assets/icon/table-bw.svg" alt="" v-show="currentTable != 1">
                        <img src="@/assets/icon/table-color.svg" alt="" v-show="currentTable == 1">
                    </div>
                    <div>
                        <div class="table-title" v-show="currentTable != 2">Стол 2</div>
                        <div class="table-title-check" v-show="currentTable == 2"> Ваш Стол 2</div>
                        <img src="@/assets/icon/table-bw.svg" alt="" v-show="currentTable != 2">
                        <img src="@/assets/icon/table-color.svg" alt="" v-show="currentTable == 2">
                    </div>
                </div>
                <div class="d-flex justify-around table-row">
                    <div>
                        <div class="table-title" v-show="currentTable != 3">Стол 3</div>
                        <div class="table-title-check" v-show="currentTable == 3"> Ваш Стол 3</div>
                        <img src="@/assets/icon/table-bw.svg" alt="" v-show="currentTable != 3">
                        <img src="@/assets/icon/table-color.svg" alt="" v-show="currentTable == 3">
                    </div>
                    <div>
                        <div class="table-title" v-show="currentTable != 4">Стол 4</div>
                        <div class="table-title-check" v-show="currentTable == 4"> Ваш Стол 4</div>
                        <img src="@/assets/icon/table-bw.svg" alt="" v-show="currentTable != 4">
                        <img src="@/assets/icon/table-color.svg" alt="" v-show="currentTable == 4">
                    </div>
                </div>
            </div>
            <div v-show="singleTable">

            </div>
        </div>
        
    </div>    
</template>

<script>
export default {
    data:function(){
        return{
            visMap:false,
            visTable:true,
            currentGuest: 'Выбери фамилию',
            currentTable: null,
            guests:[
                {name:'Выбери фамилию',table:0},
               // {name:'Гасилины',table:5},
                {name:'Даналаки | Свиридова',table:3},
                {name:'Денисова Валерия',table:2},
                {name:'Епрынцевы',table:1},
                {name:'Казьмина Яна',table:4},
                {name:'Корчагин Артем',table:3},
                {name:'Кравцов|Кондратьева',table:3},
                {name:'Кулаковы',table:4},
                {name:'Андрейщев | Медведева',table:2},
                {name:'Махров | Ненастева',table:1},
                {name:'Медведева Елизавета',table:2},
                //{name:'Медведевы',table:6},
                {name:'Павлюкова Евгения',table:1},
                {name:'Челноков Сергей',table:2},
                //{name:'Челноковы',table:6},
                {name:'Шамаевы',table:4},


            ],
        };
    },
    components:{
       // WedTabMap,
       // WedTabTable,
    },
    methods:{
         
        searchTable(){
            this.currentTable = null;
            let guest = this.guests.find(item => item.name == this.currentGuest);
            
            this.currentTable = guest.table;
            let el = document.querySelector('.table');
            var y = this.findPosY(el);
            window.scrollTo(0,y);
                    

            return this.currentTable;
        },

        findPosY(obj) {
            var curtop = 0;
            var t=1;
            if (obj.offsetParent) {
                while (t) {
                    curtop+=obj.offsetTop;
                    if (!obj.offsetParent) {
                        break;
                    }
                    obj=obj.offsetParent;
                }
            } else if (obj.y) {
                curtop+=obj.y;
            }
            return curtop;
        },

    }
}
</script>

<style scoped>

  .fade-enter-active, .fade-leave-active {
  transition: ease 5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active до версии 2.1.8 */ {
  transition: ease 5s;
}

    .table-container{
        margin: 120px 0px 40px 25px;
    }

    .table-container-title{
        margin-bottom: 30px;
    }

    .tables-wrapper{
       margin: 30px 0px 25px 0px;
    background-color: #FDE9F3;
    border-radius: 50px 0px 0px 50px;
    padding: 25px 0px 25px 25px;
    -webkit-box-shadow: -2px -5px 4px 0px rgba(92, 50, 50, 0.57);
        -moz-box-shadow:    -2px -5px 4px 0px rgba(92, 50, 50, 0.57);
        box-shadow:         -2px -5px 4px 0px rgba(92, 50, 50, 0.57);
    }

    .tabs-content{
        border: 5px solid white;
        border-radius:  25px 0px 0px 25px;
    }

    .table{
        background-color: white;
        padding: 30px;
    }
    .table-row{
        margin-top: 30px;
    }

    .table-title{
        margin-bottom: 10px;
        font-size:20px;
    }

    .guest-change{
        margin-bottom: 15px;
        margin-right: 25px;
    }

    .current-table{
        margin: 30px 0px;
       
    }

    .current-table span{
        
        font-weight: 600;
        color: white;
        background-color: #501B32;
        padding: 10px 35px;
        border-radius: 15px;
        transition: 0.7s;
        
        
    }

    .table-title-check{
        font-weight: 600;
        font-size:20px;
    }

    .guest-change div{
        margin-right: 10px;
    }

    @media screen and (min-width: 475px){
         .tabs-wrapper{
            background-color: #FDE9F3;
            padding: 50px;
            border-radius: 50px 50px 50px 50px;
        }    

    .tabs-content{
        border: 5px solid white;
        border-radius:  25px;
        padding: 60px;
        
    
    }

    .table-row img{
        width: 120px;
    }

    .table-row{
        margin-top: 20px;
    }


    .tables-wrapper{
        margin: 30px 125px;
        
        border-radius: 50px;
        padding: 25px;
        
    }

    h2{
        text-align: center;
    }

    .guest-change{
        font-size: 20px;
    }

    .current-table span{
        font-size: 28px;
    }

    .parent{
        margin-top: -80px;
    }

    }
</style>