<template>
    <div class="tab-container mt-5">
        <b-card no-body>
            <b-tabs pills card>
                <b-tab title="My debit cards" active>
                    <b-card-text>
                      <div class="white-card">
                            <div class="row">
                                <div class="col-lg-6 col-md-12 col-sm-12">
                                    <div class="left-card-main">
                                    
                                        <card />
                                    </div>

                                    <cardactionbutton />
                                </div>

                                <div class="col-lg-6 col-md-12 col-sm-12">
                                    <div class="right-card-main">
                                        <RightAccordianLayout />
                                    <p class="all-transaction">View all card transactions</p>
                                    </div>
                                </div>
                            </div>
                        </div>  
                    </b-card-text>
                </b-tab>
                <b-tab title="All company cards">
                    <b-card-text>Tab contents 2</b-card-text>
                </b-tab>
            </b-tabs>
        </b-card>
    </div>
</template>

<script>

import card from './CardContainer/card.vue'
import RightAccordianLayout from './RightAccordian/RightAccordianLayout.vue'


export default {
    name : "maintabs",
    components: {
        card,
        RightAccordianLayout,
    }
}
</script>

<style>
.tab-container .card-header {    
    background: transparent;
    padding: 0 10px;
}
.tab-container .card-header .nav-pills .nav-link{   
    color: #222222;
    opacity: 0.3;
    border-radius: 0;
    padding: 7px 0;
    font-weight: 700;
}
.tab-container .card-header .nav-pills .nav-link.active{    
    color: #222222;
    opacity: 1;
    background-color: transparent;
    
    border-bottom: 2px solid #23CEFD;
}
li.nav-item {
    margin-right: 30px;
}
.card {
    border: 0px solid rgba(0, 0, 0, 0.125) !important;
}
.card-body {    
    padding: 20px 0 !important;
}
.card-header {
    border: none !important;
}
.white-card {
    box-shadow: 1px 1px 5px 1px rgb(176 175 175 / 75%);
    -webkit-box-shadow: 1px 1px 5px 1px rgb(221 221 221 / 75%);
    -moz-box-shadow: 1px 1px 5px 1px rgba(176, 175, 175, 0.75);
    border-radius: 5px;
    padding: 50px 40px;
}.left-card-main {
    margin-top: -24px;
}
.all-transaction{
    color: #01D167;
    background: #EDFFF5;
    margin-top: -10px;
    padding: 20px 0 10px 0;
    font-size: 12px;
    border-radius: 0 0 10px 10px;
    cursor: pointer;
    border: 1px solid #DDFFEC;
}
</style>