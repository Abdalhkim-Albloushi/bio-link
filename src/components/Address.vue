<script setup>
import { ref } from "vue";

const showDetails = ref(false)

const  showDetailsToggle = ()=>{
  showDetails.value = !showDetails.value;
}

</script>

<template>
  
  <div class="address" @click="showDetailsToggle">
    <div class="header">
<div class="svg1">
  <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="currentColor" d="M14 11h7V6h-7zm3.5-1.25L15 8V7l2.5 1.75L20 7v1zM2 21q-.825 0-1.412-.587T0 19V5q0-.825.588-1.412T2 3h20q.825 0 1.413.588T24 5v14q0 .825-.587 1.413T22 21zm7-7q1.25 0 2.125-.875T12 11q0-1.25-.875-2.125T9 8q-1.25 0-2.125.875T6 11q0 1.25.875 2.125T9 14m-6.9 5h13.8q-1.05-1.875-2.9-2.937T9 15q-2.15 0-4 1.063T2.1 19"/></svg>

</div>
      <h3>Contact Details</h3>
<div v-if="!showDetails" class="svg2">
  <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="currentColor" d="M7.41 8.59L12 13.17l4.59-4.58L18 10l-6 6l-6-6z"/></svg>

</div>
<div v-else class="svg2">
<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="currentColor" d="M7.41 15.41L12 10.83l4.59 4.58L18 14l-6-6l-6 6z"/></svg>
  
</div>
    </div>

    <Transition name="slide-fade">
<div v-if="showDetails" class="body">
<div  class="items">
  <svg width="24" height="24" viewBox="0 0 24 24"  fill="currentColor" xmlns="http://www.w3.org/2000/svg">
<path fill-rule="evenodd" clip-rule="evenodd" d="M2 8C2 5.79086 3.79086 4 6 4H18C20.2091 4 22 5.79086 22 8V16C22 18.2091 20.2091 20 18 20H6C3.79086 20 2 18.2091 2 16V8ZM6 6C4.89543 6 4 6.89543 4 8V16C4 17.1046 4.89543 18 6 18H18C19.1046 18 20 17.1046 20 16V8C20 6.89543 19.1046 6 18 6H6Z" fill="#1F3447"/>
<path fill-rule="evenodd" clip-rule="evenodd" d="M6.21917 8.37534C6.56418 7.94408 7.19347 7.87416 7.62473 8.21917L12 11.7194L16.3753 8.21917C16.8066 7.87416 17.4359 7.94408 17.7809 8.37534C18.1259 8.8066 18.056 9.4359 17.6247 9.78091L12 14.2807L6.37534 9.78091C5.94408 9.4359 5.87416 8.8066 6.21917 8.37534Z" fill="#1F3447"/>
</svg>
<div class="text">
  <span>Email</span>
  <h4>abdalhkim210598@gmail.com</h4>
</div>
</div>
<div class="items">
  <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path fill-rule="evenodd" clip-rule="evenodd" d="M12.9355 6.9873C13.1413 6.47478 13.7236 6.22611 14.2361 6.43189C15.015 6.7446 15.7196 7.21726 16.3045 7.81932C16.8893 8.42137 17.3413 9.13942 17.6312 9.92707C17.822 10.4454 17.5565 11.0202 17.0383 11.211C16.52 11.4018 15.9452 11.1363 15.7544 10.618C15.5611 10.0929 15.2597 9.61421 14.8698 9.21284C14.48 8.81147 14.0102 8.49636 13.491 8.28788C12.9784 8.08211 12.7298 7.49982 12.9355 6.9873Z" fill="#1F3447"/>
<path fill-rule="evenodd" clip-rule="evenodd" d="M13.3644 3.04783C13.5073 2.51436 14.0557 2.19778 14.5891 2.34072C16.2847 2.79504 17.8308 3.68768 19.072 4.92891C20.3133 6.17014 21.2059 7.71623 21.6602 9.41179C21.8032 9.94525 21.4866 10.4936 20.9531 10.6365C20.4196 10.7795 19.8713 10.4629 19.7284 9.92943C19.3649 8.57298 18.6508 7.33611 17.6578 6.34312C16.6648 5.35014 15.428 4.63603 14.0715 4.27257C13.538 4.12963 13.2215 3.58129 13.3644 3.04783Z" fill="#1F3447"/>
<path fill-rule="evenodd" clip-rule="evenodd" d="M4.9684 5.21539C7.38659 4.40881 9.83024 5.92357 10.509 8.37601C10.9715 10.0472 10.5335 11.7995 9.46537 12.9994C9.68413 13.2827 9.92317 13.5551 10.1827 13.8148C10.4409 14.0732 10.7117 14.3114 10.9932 14.5294C12.1927 13.4528 13.9503 13.0099 15.6263 13.4744C18.0782 14.1541 19.5902 16.5996 18.7848 19.0177C18.2565 20.6043 17.2712 21.5682 15.9571 21.8855C14.7361 22.1804 13.4197 21.867 12.2585 21.3843C9.91998 20.4121 7.6108 18.4973 6.5562 17.4419C5.4767 16.3616 3.57009 14.049 2.60677 11.7149C2.1284 10.5558 1.82039 9.24419 2.1159 8.0288C2.43384 6.72121 3.3929 5.74087 4.9684 5.21539ZM8.58147 8.90949C8.16878 7.41841 6.79755 6.7136 5.60122 7.11264C4.54962 7.46337 4.18488 7.98476 4.05928 8.50132C3.91127 9.11007 4.03998 9.94505 4.45551 10.9519C5.27998 12.9496 6.98986 15.0464 7.97094 16.0282C8.92827 16.9862 11.0228 18.7047 13.0263 19.5375C14.0361 19.9573 14.8752 20.0893 15.4877 19.9414C16.0071 19.816 16.5332 19.4491 16.8873 18.3857C17.2867 17.1866 16.5807 15.8144 15.0921 15.4018C13.9842 15.0947 12.8451 15.4505 12.1672 16.1765C11.7295 16.6453 10.8951 16.9125 10.1851 16.417C9.68559 16.0683 9.2112 15.6721 8.76793 15.2285C8.32396 14.7842 7.92757 14.3086 7.57884 13.808C7.08641 13.1011 7.34917 12.2699 7.81458 11.8311C8.53521 11.1517 8.88748 10.0152 8.58147 8.90949Z" fill="#1F3447"/>
</svg>
<div class="text">
  <span>Mobile</span>
  <h4>+96897427212</h4>
</div>
</div>

<div class="items">
  <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path fill-rule="evenodd" clip-rule="evenodd" d="M12 4C10.4255 4 8.90461 4.65749 7.77503 5.84574C6.64381 7.03572 6 8.66001 6 10.3636C6 12.844 7.53632 15.2652 9.24308 17.1603C10.0789 18.0884 10.9177 18.8486 11.5484 19.3769C11.7154 19.5168 11.8673 19.64 12 19.7453C12.1327 19.64 12.2846 19.5168 12.4516 19.3769C13.0823 18.8486 13.9211 18.0884 14.7569 17.1603C16.4637 15.2652 18 12.844 18 10.3636C18 8.66001 17.3562 7.03572 16.225 5.84574C15.0954 4.65749 13.5745 4 12 4ZM12 21C11.4258 21.8187 11.4256 21.8186 11.4253 21.8184L11.4228 21.8166L11.4172 21.8127L11.3986 21.7994C11.3829 21.7882 11.3607 21.7722 11.3325 21.7517C11.2762 21.7106 11.1956 21.6511 11.0943 21.5741C10.8917 21.4203 10.6058 21.1962 10.2641 20.9101C9.58227 20.3389 8.67111 19.5139 7.75692 18.4988C5.96368 16.5076 4 13.6105 4 10.3636C4 8.16134 4.83118 6.0397 6.32548 4.46777C7.82141 2.89413 9.86146 2 12 2C14.1385 2 16.1786 2.89413 17.6745 4.46777C19.1688 6.0397 20 8.16134 20 10.3636C20 13.6105 18.0363 16.5076 16.2431 18.4988C15.3289 19.5139 14.4177 20.3389 13.7359 20.9101C13.3942 21.1962 13.1083 21.4203 12.9057 21.5741C12.8044 21.6511 12.7238 21.7106 12.6675 21.7517C12.6393 21.7722 12.6171 21.7882 12.6014 21.7994L12.5828 21.8127L12.5772 21.8166L12.5754 21.8179C12.5751 21.8181 12.5742 21.8187 12 21ZM12 21L12.5742 21.8187C12.2295 22.0604 11.7699 22.0601 11.4253 21.8184L12 21Z" fill="#1F3447"/>
<path fill-rule="evenodd" clip-rule="evenodd" d="M12 8C10.8954 8 10 8.89543 10 10C10 11.1046 10.8954 12 12 12C13.1046 12 14 11.1046 14 10C14 8.89543 13.1046 8 12 8ZM8 10C8 7.79086 9.79086 6 12 6C14.2091 6 16 7.79086 16 10C16 12.2091 14.2091 14 12 14C9.79086 14 8 12.2091 8 10Z" fill="#1F3447"/>
</svg><div class="text">
  <span>Location</span>
  <h4>sultanate of Oman- Muscat , </h4>
</div>

</div>
<button>Save to contacts</button>
</div>
</Transition>

  
</div>
</template>



<style>


.address{
    margin:16px 16px 0;

}
.address .header{
  box-sizing: border-box;
  background-color: var(--secondary-100);
  border-radius: 5px 5px 0 0;
  padding: 8px 10px ;
  position: relative;
  display: flex;
  align-items: center;
  gap: 16px;
  color: var(--secondary-400);


}

.svg2 svg, .svg1 svg{ 
width: 25px;

}
.svg2{
position: absolute;
right: 10px;
}

.address .header h3{
  font-size: 16px;
  font-weight: 500;
  letter-spacing: 1.1px;
  color: var(--background-900);

}

.address .body{
  padding-top: 20px;
  border-radius: 0px 0 15px 15px;
  background-color: var(--secondary-50);
  box-shadow: 0 1px 5px  var(--secondary-100);
color: var(--secondary-400);


}
.address  .body .items{
display: flex;

gap: 16px;
padding: 0px 10px 16px 10px;
justify-content: start;
align-items: center;

}
 .items .text {
  display: flex;
  flex-direction: column;
 justify-content: start;
 align-items: start;
 gap: 3px;
}
.items .text span{
 font-size: 12px;
 font-weight: 500;
color: var(--background-900);

 

 
}
.items .text h4{
  font-size: 14px;
  font-weight: 400;
}


.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.5s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  opacity: 0;
}
.items svg{
  width:  20px;
fill: var(--secondary-100);

}

button{
  margin: 5px auto 10px;
  padding:10px 16px;
  border: none;
  border-radius: 5px;
  font-size: 12px;
  color: var(--background-50);
  background-color: var(--secondary-700);
}
</style>