<template>
  <ion-page>    
    <ion-content> 
      <div class="flex flex-1 align-items-center">        
        
        <div class="h-1/2 w-full mt-5 bg-gray-900">
          <br><br><br><br><br><br><br><br><br><br><br><br>

            <div class="p-2 text-center">
              - Cordova Camera Plugin -
            </div>

          <br><br><br><br>
        </div>             
      </div>

      <div class="bg-white p-2">

        <p class="text-gray-500 text-xs p-2 text-center">
          <i class="fa fa-check-circle text-green-500"></i> QR Code scanned, donation ID acquired
        </p>

        <p class="text-gray-500 text-left px-2 text-sm">
          <span class="text-gray-900 font-semibold">Donor:</span> Leonard Selvaraja <br>
          <span class="text-gray-900 font-semibold">Pictures:</span> 3/12 captured <br>
        </p>        
        <div class="flex flex-1 items-center mt-2">
          <router-link to="/tabs/tab3" class="px-2 py-1 text-sm bg-gray-500 hover:bg-red-500 rounded shadow-md text-white transition duration-300 ease-in-out">
            Scan Again
          </router-link>

          <router-link to="/tabs/tab3" class="ml-2 px-2 py-1 text-sm bg-gray-500 hover:bg-red-500 rounded shadow-md text-white transition duration-300 ease-in-out">
            View Gallery
          </router-link>
        </div>


        <div class="mt-2 item-2 p-2 bg-blue-500 rounded shadow-md text-center text-white cursor-pointer">
          Capture <i class="fa fa-camera"></i>
        </div>
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
export default  {
  name: 'Tab2',
  components: { IonContent, IonPage }
}
</script>