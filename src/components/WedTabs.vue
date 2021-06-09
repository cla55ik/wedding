<template>
    <div class="tabs-container">
        <div class="tabs-wrapper">
            <div class="tabs-switch d-flex justify-around">
                <button @click="setMap">Как проехать?</button>
                <button @click="setTable">Где мой стол?</button>
            </div>  
            <div class="guest-change d-flex justify-center align-items-center" v-show="visTable">
                <div>Поиск по Имени гостя: </div>
                <select v-model="currentGuest" @change="searchTable">
                    <option v-for="(guest, index) in guests" v-bind:key="index">{{guest.name}}</option>
                </select>
            </div>
            <div class="current-table" v-show="currentTable">
                <span>Ваш стол {{currentTable}}</span> 
            </div>
            <div v-show="visMap" class="tabs-content map">
                <iframe src="https://yandex.ru/map-widget/v1/?um=constructor%3A144a77e54702f5eb17ee69aecae941469e156a928c8a246b8fd1858312349531&amp;source=constructor" width="320" height="335" frameborder="0"></iframe>
            </div>
            <div v-show="visTable" class="tabs-content table">
                <div>
                    <div class="table-title">Стол молодых</div>
                    <img src="@/assets/icon/table-main.svg" alt="">
                </div>
                <div class="d-flex justify-around table-row">
                    <div>
                        <div class="table-title">Родные Марии</div>
                        <img src="@/assets/icon/table-bw.svg" alt="" v-show="currentTable != 5">
                        <img src="@/assets/icon/table-color.svg" alt="" v-show="currentTable == 5">
                    </div>
                    <div>
                        <div class="table-title">Родные Ивана</div>
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
        </div>
        
    </div>    
</template>

<script>
//import WedTabMap from '@/components/WedTabMap.vue'
//import WedTabTable from '@/components/WedTabTable.vue'
export default {
    data:function(){
        return{
            visMap:false,
            visTable:true,
            currentGuest: 'Выбери фамилию',
            currentTable: null,
            guests:[
                {name:'Выбери фамилию',table:0},
                {name:'Гасилины',table:5},
                {name:'Даналаки|Свиридова',table:3},
                {name:'Денисова Валерия',table:2},
                {name:'Епрынцевы',table:1},
                {name:'Казьмина Яна',table:4},
                {name:'Корчагин Артем',table:3},
                {name:'Кравцов|Кондратьева',table:3},
                {name:'Кулаковы',table:4},
                {name:'Максим|Оксана',table:2},
                {name:'Махров|Ненастева',table:1},
                {name:'Медведева Елизавета',table:2},
                {name:'Медведевы',table:6},
                {name:'Павлюкова Евгения',table:1},
                {name:'Челноков Сергей',table:2},
                {name:'Челноковы',table:6},
                {name:'Шамаевы',table:4},


            ],
        };
    },
    components:{
       // WedTabMap,
       // WedTabTable,
    },
    methods:{
         setMap(){
            this.currentTable = null;
            this.visMap = true;
            this.visTable = false;
            console.log(this.visTable);
        },
        setTable(){
            this.visTable = true;
            this.visMap = false;
            console.log(this.visTable);
        },
        searchTable(){
            this.currentTable = null;
            let guest = this.guests.find(item => item.name == this.currentGuest);
            console.log(guest)

            console.log('currentGuest = '+ this.currentGuest);
            console.log('You table is ' + guest.table);

            this.currentTable = guest.table;
            return this.currentTable;
        }

    }
}
</script>

<style scoped>
    .tabs-container{
        padding-left: 30px;
        
    }

    .tabs-wrapper{
        background-color: #FDE9F3;
        padding: 30px 0px 30px 30px;
        border-radius: 50px 0px 0px 50px;
        -webkit-box-shadow: -2px -5px 4px 0px rgba(92, 50, 50, 0.57);
        -moz-box-shadow:    -2px -5px 4px 0px rgba(92, 50, 50, 0.57);
        box-shadow:         -2px -5px 4px 0px rgba(92, 50, 50, 0.57);
    }

    .tabs-switch{
        padding-right: 30px;
        padding-bottom: 20px;
    }

    .tabs-switch button{
        font-size: 18px;
        line-height: 29px;
        color: #501B32;
        background: none;
        border: none;
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
        margin-top: 60px;
    }
    }

</style>