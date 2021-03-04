<template>
  <ion-page>    
    <ion-content  class="ion-padding" :fullscreen="true">
  
      <ExploreContainer name="Tab 1 page" />

    <br><br><br><br><br><br><br><br><br><br>
      

      <center>
        <ion-button @click="openToast">Upload 240 images</ion-button>
      </center>
      <!-- <ion-button @click="openToastOptions">Open Toast: Options</ion-button> -->
    </ion-content>
  </ion-page>
</template>

<script>
import { IonButton, IonContent, IonPage, toastController } from '@ionic/vue';

export default {
  components: { IonButton, IonContent, IonPage },
  methods: {
    async openToast() {
      const toast = await toastController
        .create({
          header: 'Uploading',                    
          animated: 'true',
          message: 'Your images are queued to be uploaded..please maintain an active internet connection.',
          duration: 4000,
          cssClass: 'text-primary',
          buttons: [
            {
              text: 'Ok',
              role: 'cancel',
              handler: () => {
                console.log('Cancel clicked');
              }
            }
          ]
        })
      return toast.present();
    },
    async openToastOptions() {
      const toast = await toastController
        .create({
          header: 'Toast header',
          message: 'Click to Close',
          position: 'top',
          buttons: [
            {
              side: 'start',
              icon: 'star',
              text: 'Favorite',
              handler: () => {
                console.log('Favorite clicked');
              }
            }, {
              text: 'Done',
              role: 'cancel',
              handler: () => {
                console.log('Cancel clicked');
              }
            }
          ]
        })
      return toast.present();
    },
  },
}
</script>
<style scoped>
  .text-primary {
    color: gray;
  }
</style>