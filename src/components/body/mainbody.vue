<template>
    <div class="main-content">
            <div class="create" data-view-active="true">
                <div class="row">
                    <div class="col-12 col-lg-12 col-md-12 col-sm-12">
                        <div class="row top-section">
                            <div class="col col-lg-6 col-md-6 col-sm-6">
                                <div class="left-head">
                                    <p>Available balance</p>
                                    <h3>
                                        <span class="green">S$</span>
                                        <span>3000</span> 
                                        </h3>
                                </div>
                            </div>
                            <div class="col col-lg-6 col-md-6 col-sm-6 right-head-main">
                                <div class="right-head">
                                    <div class="mobile-logo">
                                        <img src="../../assets/images//Logo.png" >
                                    </div>
                                    <button v-b-modal.modal-1 class="btn btn-primary modalbtn"><img src="../../assets/images//box.png">New card</button>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="col-12 col-lg-12 col-md-12 col-sm-12">
                        <maintabs />
                    </div>
                    <createusermodal />
                </div>

            </div>
        </div>
</template>
<script>
import maintabs from './maintabs.vue'
import createusermodal from './CardContainer/createusermodal.vue'

export default {
    name: "mainbody",
    components: {
        maintabs,
        createusermodal,
    }
}
</script>

<style>

.main-content {
    min-height: 100vh;
    margin-left: 20rem;
    padding: 3rem;
}
.btn-primary {
    color: #fff;
    background-color: #325BAF;
    border-color: #325BAF;
}
.right-head-main {
    display: flex;
    justify-content: flex-end;
    align-items: center;
}
.left-head h3 span.green {
    font-size: 18px;
    color: #fff;
    background: #01d167;
    padding: 2px 10px;
    border-radius: 5px;
}
.left-head h3 span {
    font-size: 19px;
    padding: 2px 10px;
    border-radius: 5px;
}
.left-head p {
    font-size: 13px;
}
.left-head {
    float: left;
}.left-head h3 {
    font-weight: 600;
}
.modalbtn {
    background: #325BAF !important;
}
.modalbtn img{
    margin-right: 10px;
}
.mobile-logo{
    display: none;
    margin-bottom: 20px;
}
</style>