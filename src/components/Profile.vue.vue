<template>

<div v-if="!isLoading" class="profile">

<Avatar/>
<p>
مبرمج مواقع والتطبيقات, خبره في مجال برمجة المواقع والتطبيقات
</p>
<h1>عبدالحكيم علي البلوشي</h1>
<MedialIconsVue />



<div class="details">

  <div class="share"></div>
  <Address />
<Location />
  <ImageSlider />
  <div class="loction"></div>
</div>


</div>
<div v-else>
  <SplashView />
</div>






</template>

<script setup>
import { onMounted, ref } from 'vue';

import Avatar from './Avatar.vue';
import MedialIconsVue from './MedialIcons.vue';
import SplashView from './SplashView.vue'
import Address from './Address.vue';
import Location from './Location.vue';
import ImageSlider from './ImageSlider.vue'
const isLoading = ref(true)




onMounted(()=>{
      setTimeout(() => {
            isLoading.value = false
            }, 1000);
      });

</script>

<style scoped>
.profile{
  width: 100%;
}


.profile h1 {
  font-size: 18px;
  font-weight: bold;

}
.profile p, .profile h1 
{
  font-family: Helvetica, Arial;
  direction: rtl;

  
}
.profile p{
  color: var(--text-800);
  opacity: 0.4;
  width: 75%;
  font-weight: 400;
  margin:10px auto ;
  text-align: center;
  

}

.profile .details{

}

</style>
