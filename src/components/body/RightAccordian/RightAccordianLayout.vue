<template>
  <div class="accordion" role="tablist">


    <b-card no-body class="mb-1 right-accordian">
      <b-card-header header-tag="header" class="p-1 head-container" role="tab">
            <b-button class="accordian-head" block v-b-toggle.accordion-1 variant="info">
            <img src="../../../assets/images/Group 11889.png"> Card details</b-button>
      </b-card-header>
      <b-collapse id="accordion-1" accordion="my-accordion" role="tabpanel">
        <b-card-body>
          <b-card-text>{{ textCardDetail }}</b-card-text>
        </b-card-body>
      </b-collapse>
    </b-card>



    <b-card no-body class="mb-1 right-accordian">
      <b-card-header header-tag="header" class="p-1 head-container" role="tab">
        <b-button class="accordian-head" block v-b-toggle.accordion-2 variant="info"><img src="../../../assets/images/Group 11889-e.png"> Recent transactions</b-button>
      </b-card-header>
      <b-collapse id="accordion-2" visible accordion="my-accordion" role="tabpanel">
        <b-card-body>
         <RecentTransactions />         
        </b-card-body>
      </b-collapse>
    </b-card>



  </div>
</template>

<script>
import RecentTransactions from './RecentTransactions.vue'

  export default {
      name : 'RightAccordianLayout',
      components: {
        RecentTransactions,
      },
    data() {
      return {
        textCardDetail: `
          Card Detail content 
        `
      }
    }
  }
</script>

<style>
.accordion .right-accordian {
    border: 1px solid #F0F0F0 !important;
    border-radius: 8px !important;    
}
.accordion .right-accordian .head-container .accordian-head{
    overflow-anchor: none;
    background: #F5F9FF;
    color: #0C365A;
    height: 72px;
    border-radius: 10px;
    border: none;
    box-shadow: none;
    text-align: left;
    padding: 0 25px;
    box-shadow: 1px 1px 5px 1px rgb(176 175 175 / 75%);
    -webkit-box-shadow: 1px 1px 5px 1px rgb(221 221 221 / 75%);
    -moz-box-shadow: 1px 1px 5px 1px rgba(176, 175, 175, 0.75);
}
.accordion .right-accordian .head-container .accordian-head img{    
    margin-right: 10px;
}
.accordion .right-accordian .head-container{
    
    padding: 0 !important;
    margin: 0;
    background-color: transparent;
    border-bottom: none;
}

</style>