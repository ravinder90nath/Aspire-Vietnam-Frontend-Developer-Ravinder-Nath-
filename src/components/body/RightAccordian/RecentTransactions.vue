<template>
    <div class="notification-container">
        <b-card>
            <b-media>
                <template #aside>
                    <span class="lefticn"><img src="../../../assets/images/file-storage.png"></span>
                </template>

                <h5 class="mt-0 title">Hamleys</h5><span>+ S$ 150</span>
                <p class="date">20 May 2020</p>
                <div class="group-container"><p><span><img src="../../../assets/images/business-and-finance.png"></span>+ S$ 150</p></div>
            </b-media>
        </b-card>
    </div>
</template>

<script>
export default {
    name: "RecentTransactions",
}
</script>

<style>
.notification-container{
    padding: 20px;
}

.notification-container .card{
    border-bottom: 1px solid #F5F5F5 !important;
}
span.lefticn {
    padding: 10px 15px;
    background: #009DFF1A;
    border-radius: 40px;
}
.notification-container .title {
    text-align: left;
    color: #222222;
    font-size: 15px;
    font-weight: 700;
    float: left;
}
</style>