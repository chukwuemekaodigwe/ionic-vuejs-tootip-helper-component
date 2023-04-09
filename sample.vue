<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-img src="/vite.svg" class="ion-align-self-end"></ion-img>
        </ion-buttons>
        <ion-title> New SignUp</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content>
      <ion-grid>
        <ion-row>
          <ion-col size="8" offset="2">

            <ion-list inset="true">
              <form @submit.prevent="handleSignup">
                <ion-item>

                  <ion-label position="stacked"> Company Name</ion-label>
                  <ion-input type="text" v-model="form.company" autocomplete></ion-input>
                </ion-item>
                <ion-item>
                  <ion-label position="stacked"> Company Address </ion-label>
                  <tooltip for="address" position="start" bg-color="darkblue" icon-color="blue" text-color="white"
                    message="write on the company address" :is-outline="true"></tooltip>
                  <ion-input v-model="form.address" autocomplete type="text"></ion-input>
                </ion-item>
                <ion-row class="bordered">
                  <ion-col size-md="6">
                    <ion-item>
                      <ion-label position="stacked"> Business Email </ion-label>


                      <tooltip for="email" font-size="36px" bg-color="darkblue" icon-color="blue" text-color="white"
                        message="write on the company address" :is-outline="false"></tooltip>
                      <ion-input type="email" v-model="form.email" autocomplete></ion-input>

                    </ion-item>
                  </ion-col>
                  <ion-col size-md="6">
                    <ion-item>
                      <ion-label position="stacked">Company Phone N&otilde; </ion-label>

                      <ion-input type="tel" v-model="form.phone" autocomplete></ion-input>

                    </ion-item>
                  </ion-col>
                </ion-row>
                <ion-row>
                  <ion-col size="4" offset="3">
                    <tooltip for="button" message="Click submit button to continue" icon-color="darkblue" bg-color="black"
                      text-color="white"></tooltip>
                    <ion-button type="submit" color="danger" expand="block">Sign Up</ion-button>
                    <a href="/login"> Login Instead</a>

                  </ion-col>

                </ion-row>
              </form>
            </ion-list>

          </ion-col>
        </ion-row>
      </ion-grid>
    </ion-content>

  </ion-page>
</template>
  
  
<script lang="ts">
import {
  IonButtons,
  IonButton,
  IonPage,
  IonHeader,
  IonContent,
  IonToolbar, IonList,
  IonTitle,

} from "@ionic/vue";
import { defineComponent, ref, reactive, onMounted, inject } from "vue";
import tooltip from "./ionic-tooltip.vue";


export default defineComponent({
  name: 'signupPage',

  components: {
    IonButtons,
    IonButton,
    IonPage,
    IonHeader,
    IonContent,
    IonToolbar, IonList,
    tooltip
  },

  setup(props) {

    let form = reactive({
      company: '',
      address: '',
      email: '',
    })

    return {
      form
    }
  }

});

</script>
  
<style>
.bordered {
  border-bottom: .7px solid #eee;
}

::placeholder {
  font-size: smaller;
  font-style: italic;
}
</style>