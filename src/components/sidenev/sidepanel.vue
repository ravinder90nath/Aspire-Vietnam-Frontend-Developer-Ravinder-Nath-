<template>
  <div>
    <!-- <b-button v-b-toggle.sidebar-variant>Toggle Sidebar</b-button> -->
    <b-sidebar class="container-sidebar" text-variant="light" visible no-header shadow >
      <div class="px-5 py-5">
        <div class="main-logo-container">
            <img src="../../assets/images/Aspire Logo.png">

            <p>Trusted way of banking for 3,000+ SMEs and startups in Singapore</p>

            <b-list-group class="nev-panel">
                <b-list-group-item class="d-flex align-items-center">
                    <img src="../../assets/images/Home.png">
                    <span class="mr-auto">Home</span>
                </b-list-group-item>
                <b-list-group-item class="d-flex align-items-center active">
                    <img src="../../assets/images/Card.png">
                    <span class="mr-auto">Cards</span>
                </b-list-group-item>
                <b-list-group-item class="d-flex align-items-center">
                    <img src="../../assets/images/Payments.png">
                    <span class="mr-auto">Payments</span>
                </b-list-group-item>
                <b-list-group-item class="d-flex align-items-center">
                    <img src="../../assets/images/Credit.png">
                    <span class="mr-auto">Credit</span>
                </b-list-group-item>
                <b-list-group-item class="d-flex align-items-center">
                    <img src="../../assets/images/Account.png">
                    <span class="mr-auto">Settings</span>
                </b-list-group-item>
            </b-list-group>
        </div>

        
        
      </div>
    </b-sidebar>
  </div>
</template>

<script>
export default {
    name: "sidepanel",
}
</script>


<style>
.container-sidebar .b-sidebar-body{    
    background-color: #0C365A;
}
.main-logo-container {
    float: left;
    text-align: left;
}

.main-logo-container p{
    color: #fff;
    opacity: 0.3;
    font-size: 14px;
    margin: 20px 0;
}

.nev-panel > div{
    background-color: transparent;
    padding: 22px 0px;
    border: none;
    font-size: 15px;
}
.nev-panel > div.active{
    background-color: transparent;
    color: #01D167;
}
.nev-panel > div img{
    margin-right: 20px;
}
</style>