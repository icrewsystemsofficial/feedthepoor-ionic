<template>
  <ion-page>    
    
    <ion-content>                

      <br><br><br>
      <ion-card>
            <ion-card-content>                            
              <ion-text>
                <!-- <ion-icon size="small" :icon="locationOutline" /> -->
                 <strong>NGO:</strong>
              </ion-text>

              <span class="trust-name">              
                Roshni Charitable Trust
              </span>              
            </ion-card-content>            
          </ion-card>            

          <div class="bg-green-500">
            <div class="max-w-7xl mx-auto py-3 px-3 sm:px-6 lg:px-8">
              <div class="flex items-center justify-between flex-wrap">
                <div class="flex-1 flex items-center mb-2">                  
                  <p class="text-white text-sm">
                    <i class="fa fa-check-circle text-green-200"></i> 40 pictures clicked, ready for upload</p>
                </div>
                
                  <router-link to="/tabs/tab3"  class="flex  w-full items-center justify-center p-1 border border-transparent rounded-md shadow-sm text-sm font-medium text-green-600 bg-white hover:bg-green-50">
                    Upload
                  </router-link>                   
              </div>
            </div>
          </div>


          <ion-list class="ion-padding">          
            <ion-item button @click="buttonClick()">
              <ion-label>
                Leonard Selvaraja (12 meals)
              </ion-label>
            </ion-item>

            <ion-item button @click="buttonClick()">
              <ion-label>
                Ayshwaria Grace (14 meals)
              </ion-label>
            </ion-item>

            <ion-item button @click="buttonClick()">
              <ion-label>
                Samay Bhattacharya (10 meals)
              </ion-label>
            </ion-item>

            <!-- Item as an Anchor -->
            <!-- <ion-item href="https://www.ionicframework.com">
              <ion-label>
                Anchor Item
              </ion-label>
            </ion-item> -->

            <ion-item color="danger" style="border-radius: 5px;">
              <ion-label>
                36 pictures to be clicked
              </ion-label>
            </ion-item>            
 
          </ion-list>

          <!-- <ion-text>
            <p class="p-2 text-white text-center text-sm">40 pictures ready to be uploaded</p>
          </ion-text> -->

          <center>
            <br>
            <router-link to="/tabs/tab2" class="px-2 py-1 bg-blue-500 text-white font-light rounded shadow-md">
              Start Capturing
            </router-link>
          </center>
      

      <!-- <ExploreContainer name="Tab 1 page" /> -->
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonContent,IonList, IonItem, toastController } from '@ionic/vue';
// import ExploreContainer from '@/components/ExploreContainer.vue';

export default  {
  name: 'Tab1',
  components: { IonContent, IonPage, IonList, IonItem } ,
  methods: {
    async openToast() {
      const toast = await toastController
        .create({
          header: 'Uploading',                              
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