<script setup>
import { ref } from "vue";

const showDetails = ref(false)

const  showDetailsToggle = ()=>{
  showDetails.value = !showDetails.value;
}

</script>

<template>
  
  <div class="loction" @click="showDetailsToggle">
    <div class="header">
<div class="svg1">
  <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="currentColor" d="M12 20.556q-.235 0-.47-.077q-.234-.077-.432-.25q-1.067-.98-2.163-2.185q-1.097-1.204-1.992-2.493q-.895-1.29-1.467-2.633q-.572-1.343-.572-2.622q0-3.173 2.066-5.234Q9.037 3 12 3t5.03 2.062q2.066 2.061 2.066 5.234q0 1.279-.572 2.613q-.572 1.333-1.458 2.632q-.885 1.3-1.981 2.494q-1.097 1.194-2.164 2.175q-.198.173-.442.26q-.244.086-.479.086m0-6.056q1.13 0 2.073-.514q.942-.515 1.554-1.37q-.779-.553-1.696-.834Q13.013 11.5 12 11.5t-1.93.282q-.918.281-1.697.833q.612.856 1.554 1.37q.942.515 2.073.515m0-5q.633 0 1.066-.434Q13.5 8.633 13.5 8t-.434-1.066Q12.633 6.5 12 6.5t-1.066.434Q10.5 7.367 10.5 8t.434 1.066Q11.367 9.5 12 9.5"/></svg>
</div>
      <h3>Office Location</h3>
<div v-if="!showDetails" class="svg2">
  <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="currentColor" d="M7.41 8.59L12 13.17l4.59-4.58L18 10l-6 6l-6-6z"/></svg>

</div>
<div v-else class="svg2">
<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="currentColor" d="M7.41 15.41L12 10.83l4.59 4.58L18 14l-6-6l-6 6z"/></svg>
  
</div>
    </div>

    <Transition name="slide-fade">
<div v-if="showDetails" class="body">
  <img src="../assets//map.png" alt="">
</div>

</Transition>

  
</div>
</template>



<style>

.loction{
  margin:16px 16px 0;
}
.loction .header{
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

.loction .header h3{
  font-size: 16px;
  font-weight: 500;
  letter-spacing: 1.1px;
  color: var(--background-900);

}

.loction .body{
border-radius: 0px 0 15px 15px;
background-color: var(--secondary-50);
box-shadow: 0 1px 5px  var(--secondary-100);
color: var(--secondary-400);
width: 100%;


}
.loction .body img{
  width: 100%;
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