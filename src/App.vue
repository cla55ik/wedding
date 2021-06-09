<template>
 
  
  
  <Header
    
  />
  <Introduction

  />

  <Address
  />

  <Map
  />

  <MyTable
  />

  <Plan
  />

  <Foot
  />

  
</template>

<script>

import Header from '@/components/Header.vue'
import Address from '@/components/Address.vue'
//import WedTabs from '@/components/WedTabs.vue'
import Introduction from '@/components/Introduction.vue'
import Map from '@/components/Map.vue'
import MyTable from '@/components/MyTable.vue'
import Plan from '@/components/Plan.vue'
import Foot from '@/components/Foot.vue'

export default {
  name: 'App',
  components: {
    
    Header,
    Address,
    //WedTabs,
    Introduction,
    Map,
    MyTable,
    Plan,
    Foot,
  },
  data(){
    return{
      todos: [
        {id:1, title: 'Купить Хлеб', complined: false},
        {id:2, title: 'Купить Молоко', complined: false},
        {id:3, title: 'Купить Мясо', complined: false},
        {id:4, title: 'Купить Сумку', complined: false},
      ],
      
    }
  }
}
</script>

<style>

@font-face {
    font-family: "Yanone";
    src: local("Yanone"),
    url("~@/fonts/YanoneKaffeesatz-Regular.ttf") format("truetype");
    
    font-display: auto;

}


@font-face {
  font-family: "Caslon";
  src: local("Caslon"), 
  url("~@/fonts/Caslon_Becker_No540.ttf") format("truetype");
  
  font-display: auto;
  
  
}


#app {
  font-family: Yanone, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #501B32;
  
}

#app .title-names{
        font-family: 'Caslon';
        
        font-size: 36px;
        line-height: 43px;        
    }
</style>
