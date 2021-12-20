<template>
    <div class="notification-container">
        <b-card>
            <b-media>
                <template #aside>
                    <span class="lefticn"><img src="../../../assets/images/file-storage.png"></span>
                </template>

                <h5 class="mt-0 title">Hamleys</h5>
                <p class="amount">+ S$ 150</p>
                <p class="date">20 May 2020</p>
                <div class="group-container"><p><span><img src="../../../assets/images/business-and-finance.png"></span>Refund on debit card</p></div>
            </b-media>
        </b-card>
        <b-card>
            <b-media>
                <template #aside>
                    <span class="lefticn"><img src="../../../assets/images/flights.png"></span>
                </template>

                <h5 class="mt-0 title">Hamleys</h5>
                <p class="amount">+ S$ 150</p>
                <p class="date">20 May 2020</p>
                <div class="group-container"><p><span><img src="../../../assets/images/business-and-finance.png"></span>Refund on debit card</p></div>
            </b-media>
        </b-card>
        <b-card>
            <b-media>
                <template #aside>
                    <span class="lefticn danger"><img src="../../../assets/images/megaphone.png"></span>
                </template>

                <h5 class="mt-0 title">Hamleys</h5>
                <p class="amount">+ S$ 150</p>
                <p class="date">20 May 2020</p>
                <div class="group-container"><p><span><img src="../../../assets/images/business-and-finance.png"></span>Refund on debit card</p></div>
            </b-media>
        </b-card>
        <b-card>
            <b-media>
                <template #aside>
                    <span class="lefticn"><img src="../../../assets/images/file-storage.png"></span>
                </template>

                <h5 class="mt-0 title">Hamleys</h5>
                <p class="amount">+ S$ 150</p>
                <p class="date">20 May 2020</p>
                <div class="group-container"><p><span><img src="../../../assets/images/business-and-finance.png"></span>Refund on debit card</p></div>
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
    padding: 0 20px;
}

.notification-container .card{
    border-bottom: 1px solid #F5F5F5 !important;
}
span.lefticn {
    padding: 10px 15px;
    background: #009DFF1A;
    border-radius: 40px;
}
span.lefticn.danger {
    background: #F251951A;
}
.notification-container .title {
    text-align: left;
    color: #222222;
    font-size: 15px;
    font-weight: 700;
    float: left;
    margin: 0;
}

.media-body p.amount{
    color: #01D167;
    font-weight: 700;
    text-align: right;
    margin: 0;
}
.media-body p.date{
    color: #AAAAAA;
    margin: 0;
    text-align: left;
}.group-container {
    float: left;
    margin-top: 10px;
}
.group-container p {
    color: #325BAF;
    font-size: 13px;
    font-weight: 700;
    margin: 0;
}
.group-container span {
    background: #325BAF;
    padding: 4px 9px;
    margin-right: 10px;
    border-radius: 20px;
}

</style>