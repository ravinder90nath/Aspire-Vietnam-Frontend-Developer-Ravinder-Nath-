
<template>
  <div class="card-slider">
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Text slides with image -->
      <b-carousel-slide v-for="item in list" v-bind:key="item.id">
          <p class="showbtn"><img src="../../../assets/images/remove_red_eye-24px.png"> Show card number</p>
            <div class="green-card " :class="item.active==1?'active-card':'inactive-card'" >
                <div class="main-card">
                    <div class="logo-img">
                        <img src="../../../assets/images/Home.png" class="img-fluid"> aspire
                    </div>
                    <h3 class="username">{{item.username}}</h3>
                    <div class="circle">
                        <p>{{item.cardnumber}}</p> 
                    </div>
                    <div class="circle1">
                        <p>Thru: <span>{{item.expmonth}} / {{item.expyear}}</span></p>
                        <p>CVV: <span>***</span></p>
                    </div>
                    <div class="visa-img">
                        <img src="../../../assets/images/Visa Logo.png" class="img-fluid"> 
                    </div>
                </div>
            </div>
            
            <div class="action-btn">
                <!-- Image and text -->
                <b-navbar variant="faded" type="light">
                    <b-navbar-brand>
                        <img src="../../../assets/images/ActionBtn/Freeze card.png" class="d-inline-block align-top" alt="Kitten">
                        <p>Freeze card</p>
                    </b-navbar-brand>
                    <b-navbar-brand>
                        <img src="../../../assets/images/ActionBtn/Set spend limit.png" class="d-inline-block align-top" alt="Kitten">
                        <p>Set spend limit</p>
                    </b-navbar-brand>
                    <b-navbar-brand>
                        <img src="../../../assets/images/ActionBtn/GPay.png" class="d-inline-block align-top" alt="Kitten">
                        <p>Add to GPay</p>
                    </b-navbar-brand>
                    <b-navbar-brand>
                        <img src="../../../assets/images/ActionBtn/Replace card.png" class="d-inline-block align-top" alt="Kitten">
                        <p>Replace card</p>
                    </b-navbar-brand>
                    <b-navbar-brand v-on:click="deleteUser(item.id)">
                        <img src="../../../assets/images/ActionBtn/Deactivate card.png" class="d-inline-block align-top" alt="Kitten">
                        <p>Cancel card</p>
                    </b-navbar-brand>
                </b-navbar>
            </div>
      </b-carousel-slide>
    </b-carousel>

    
            

  </div>
</template>

<script>
import Vue from 'vue';
import VueAxios from 'vue-axios';
import axios from 'axios';

Vue.use(VueAxios, axios);

export default {
    name: "card",
    data(){
        return{
            list:undefined,
        }
    },
    methods:{
        getUsers(){
            this.axios.get('http://localhost:3000/usercard').then((resp)=>{
            this.list=resp.data
            console.warn(resp.data)
        })
        },

        deleteUser(id){
            this.axios.delete('http://localhost:3000/usercard/'+id).then((resp)=>{
            this.getUsers()
            console.warn(resp.data)
        })
        }
    },
    mounted(){
        this.getUsers()
        // Vue.axios.get('http://localhost:3000/usercard')
        // .then(resp=>{
        //     this.list=resp.data
        //     console.warn(resp.data)
        // })
    }
}
</script>

<style>
.green-card {
    background: #01D167;
    border-radius: 25px;
    padding: 20px;
    color: #fff;
}
.green-card .active-card{
    
    background: #01D167;
}
.inactive-card{

    background: #ff0000;
}
.logo-img {
    display: flex;
    justify-content: flex-end;
}
.logo-img img {
    margin-right: 5px;
}
.circle, .circle1 {
    display: flex;
}
.circle p {
    margin: 10px 30px 10px 0;
    font-size: 17px;
    font-weight: 600;
}
.circle1 p {
    margin-right: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 15px;
    font-weight: 700;
}
.circle1 p span{
    margin-left: 20px;
    font-size: 17px;
}
.username{
    text-align: left;
    font-weight: 600;
}.visa-img {
    text-align: right;
}

.card-slider .carousel-caption {
    position: initial;
    padding: 0;
    }
    .card-slider .carousel {
    text-shadow: none !important;
    background: transparent;
    border-radius: 60px;
}

.card-slider .carousel-indicators {
    bottom: 160px;
}
    .card-slider .carousel-indicators li {
    width: 8px;
    height: 8px;
    border-radius: 8px;
    background-color: #01D167;
    }
  .card-slider .carousel-indicators li.active {
    width: 16px;
    }
    .card-slider .carousel-item {
    border-radius: 25px;
}
.card-slider .carousel-item, .card-slider .carousel {
    background: transparent !important;
}
.action-btn {
    background: #EDF3FF;
    margin-top: 60px;
    border-radius: 25px;
    padding: 20px 0px;
}
a.carousel-control-prev, .carousel-control-next {
    display: none !important;
}
.action-btn .navbar-brand {
    width: 20%;
    margin: 0;
    cursor: pointer;
}
.action-btn .navbar-brand p{
    color: #0C365A !important;
    font-size: 14px;
    font-weight: 600;
    white-space: break-spaces;
    margin: 0;
}
.action-btn .navbar-brand img {
    margin-bottom: 10px;
}
.showbtn{
    color: #01D167;
    font-size: 12px;
    font-weight: 600;
    margin: 3px 0px;
    text-align: right;
}
</style>