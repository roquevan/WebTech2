<template>
  <ion-page>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Blank</ion-title>
        </ion-toolbar>
      </ion-header>
    
      <div id="container">
        <strong>Welcome</strong>
        <p>Start with Trafex by <br> Logging in as.</p>
      </div>
    </ion-content>
  </ion-page>

  <div id="loginButton">
    <ion-button color="dark">Individual</ion-button>
    <ion-button color="dark">Establishment</ion-button>
  </div>
</template>

<script lang="ts">
import { IonContent, IonPage, IonToolbar, IonButton } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Home',
  components: {
    IonContent,
    IonPage,
    IonToolbar,
    IonButton
  }
});
</script>

<style scoped>
#container {
  text-align: center;
  
  position: absolute;
  left: 0;
  right: 0;
  top: 30%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 40px;
}

#container p {
  font-size: 20px;
  line-height: 22px;
  font-weight: lighter;
  color: #8c8c8c;
  
  margin: 0;
}

#container a {
  text-decoration: none;
}

#loginButton{
  position: absolute;
  width: 90%;
  top: 300px;
   border-radius: 2px;
   margin-left: 50px;
   margin-top: auto;
}

#loginButton ion-button{
  width: 40%;
  box-shadow: none;
  text-transform: initial;
  height: 50px;
}
</style>