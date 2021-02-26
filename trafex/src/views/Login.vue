<template>
<div id="container">
    <strong>Trafex</strong>
    <p>Covid-19 Contact Tracing App</p>
</div>
<div id="form">
<p>Sign in to Continue</p>
</div>
  <ion-content class="ion-padding ion-text-center">
      <ion-item lines="none">
          <ion-input placeholder="Enter Phone Number"></ion-input>
      </ion-item>
      <ion-item lines="none">
          <ion-input placeholder="Password" type="password"></ion-input>
      </ion-item>
      <div id="forgotButton">
          <ion-button fill="clear" expand="block">Forgot Password</ion-button>
      </div>

      <ion-button color="dark" expand="block">Login</ion-button>
      <div id="new">
      <ion-button fill="clear" expand="block">New User? Sign Up</ion-button>
      </div>
  </ion-content>
</template>

<script>
import { IonContent, IonButton, IonItem, IonInput} from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Home',
  components: {
    IonContent,
    IonButton,
    IonItem,
    IonInput
  }
});
</script>

<style scoped>
#container
{
    text-align: center;
    

}
#container strong {
  font-size: 50px;
  line-height: 70px;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
}

#container p{
    font-size: 20px;
    margin-top: -15px;
}


#form{
    font-family: monospace;
    font-size: 18px;
    margin-left: 10px;
    margin-bottom: -15px;
    color: grey;
}
ion-item{
    border-style: solid;
    margin-bottom: 10px;
    border-color: rgb(201, 201, 201);
    border-width: 2px;
    border-radius: 7px;
}

ion-button{
    height: 50px;
    border-width: 2px;
    margin-top: 20px;
}
#forgotButton ion-button{
    margin-left: auto;
    margin-top: 20px;
    margin-bottom: 5px;
    width: fit-content;
    height: fit-content;
    border-radius: 30px;
}

#new ion-button{
    height: fit-content;
    width: fit-content;
    margin-left: auto;
    margin-right: auto;
    border-radius: 30px;
}


</style>