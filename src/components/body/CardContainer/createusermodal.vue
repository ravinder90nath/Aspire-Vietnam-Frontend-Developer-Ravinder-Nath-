<template>
    <div>
        <b-modal id="modal-1" ref="modal1" title="Create User" hide-footer>
            <form @submit="submitData" method="POST">
              <b-form-group label="Email address:" label-for="inline-form-input-name">
                  <b-form-input name="username" v-model="post.username" id="inline-form-input-name" class="mb-2 mr-sm-2 mb-sm-0" placeholder="User Name" ></b-form-input>
              </b-form-group>

              <input type="hidden" name="date" v-model="post.expmonth" class="mb-2 mr-sm-2 mb-sm-0" placeholder="expdate" >
              <input type="hidden" name="date" v-model="post.expyear" class="mb-2 mr-sm-2 mb-sm-0" placeholder="expdate" >
              <input type="hidden" name="cardnumber" v-model="post.cardnumber" v-mask="`#### - #### - #### - ####`" class="mb-2 mr-sm-2 mb-sm-0" placeholder="cardnumber" >

              <b-button class="float-right" type="submit" @click="hideModal" ariant="primary">Save</b-button>
            </form>
        </b-modal>
    </div>
</template>

<script>
import Vue from 'vue';
import VueAxios from 'vue-axios';
import axios from 'axios';

Vue.use(VueAxios, axios);

export default {
    name: "createusermodal",
    data(){
      return{
        post:{
          username: null,
          expmonth: Math.floor(1 + Math.random() * 12),
          expyear: Math.floor(2021 + Math.random() * 30),
          cardnumber: Math.floor(1000000000000000 + Math.random() * 9000000000000000),
          active: true,
          removecard: true,
        }

      }
    },

    methods: {
      hideModal() {
        this.$refs.modal1.hide();
      },

      submitData(e){
        this.axios.post('http://localhost:3000/usercard', this.post).then((result)=>{
          
          console.warn("result", result)
        })
          console.warn(this.post)
          e.preventDefault();
      }
    }
   
}
</script>
