<template>
  <ion-page>  
    <ion-header>
      <ion-toolbar>        
        <ion-title>
          <center>            
            <small>#feedThePoor <strong>Voulunteer</strong></small>
          </center>                    
        </ion-title>                
      </ion-toolbar>
    </ion-header>
    


    <ion-tabs>
      <ion-tab-bar slot="bottom">
        <ion-tab-button tab="tab1" href="/tabs/tab1">
          <ion-icon :icon="home" />
          <!-- <ion-label>Home</ion-label> -->
        </ion-tab-button>
          
        <ion-tab-button tab="tab2" href="/tabs/tab2">
          <ion-icon :icon="camera" />          
        </ion-tab-button>
        
        <ion-tab-button tab="tab3" href="/tabs/tab3">
          <ion-icon :icon="cloudUpload" />          
        </ion-tab-button>
      </ion-tab-bar>
    </ion-tabs>
  </ion-page>
</template>

<script lang="ts">
import { IonTabBar, IonTabButton, IonTabs, IonIcon, IonPage } from '@ionic/vue';
import { camera, cloudUpload, home, locationOutline} from 'ionicons/icons';

export default {
  name: 'Tabs',
  components: { IonTabs, IonTabBar, IonTabButton, IonIcon, IonPage },
  setup() {
    return {
      cloudUpload, 
      camera,            
      home,
      locationOutline,
    }
  }
}
</script>
<style>

  .trust-name {
    font-size: 12px;
    align-content: left;
  }

  ion-header {
  --background: linear-gradient(162deg, rgba(56, 70, 108, .8) 20%, rgba(56, 70, 108, .8) 100%), url('https://www.nexiga.com/geomarketing-blog/wp-content/uploads/2017/11/shutterstock_654668191_Parkhaus.jpg') bottom no-repeat;
  }

  ion-content{
    --background: linear-gradient(162deg, rgba(56, 70, 108, .8) 20%, rgba(56, 70, 108, .8) 100%), url('https://www.nexiga.com/geomarketing-blog/wp-content/uploads/2017/11/shutterstock_654668191_Parkhaus.jpg') bottom no-repeat;
/* --background: #fff url('https://t4.ftcdn.net/jpg/02/17/89/41/360_F_217894165_H4jRalQ4eg9Kp8XUVGEa7XFDEPtTQ9PY.jpg') no-repeat center center / cover; */
}
</style>