<template>
<div class="avatar">
    <div class="icon">
      <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 16 16"><path fill="currentColor" fill-rule="evenodd" d="M8.75 2.25a.75.75 0 0 0-1.5 0v5h-5a.75.75 0 0 0 0 1.5h5.5a1 1 0 0 0 1-1zM7.25 11a1 1 0 0 1 1-1H11a.75.75 0 0 1 0 1.5H8.75v2.25a.75.75 0 0 1-1.5 0zM13 13h-2.25a.75.75 0 0 0 0 1.5h2.75a1 1 0 0 0 1-1V8.25a1 1 0 0 0-1-1h-2.75a.75.75 0 0 0 0 1.5H13zM3 4.5V3h1.5v1.5zm-1.5-2a1 1 0 0 1 1-1H5a1 1 0 0 1 1 1V5a1 1 0 0 1-1 1H2.5a1 1 0 0 1-1-1zm1.5 9V13h1.5v-1.5zM2.5 10a1 1 0 0 0-1 1v2.5a1 1 0 0 0 1 1H5a1 1 0 0 0 1-1V11a1 1 0 0 0-1-1zm9-5.5V3H13v1.5zm-1.5-2a1 1 0 0 1 1-1h2.5a1 1 0 0 1 1 1V5a1 1 0 0 1-1 1H11a1 1 0 0 1-1-1z" clip-rule="evenodd"/></svg>

    </div>
    <div class="img"><img :src="myImge" alt="Image" loading="lazy"></div>
   <div class="icon">
    <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12a3 3 0 1 0 6 0a3 3 0 1 0-6 0m12-6a3 3 0 1 0 6 0a3 3 0 1 0-6 0m0 12a3 3 0 1 0 6 0a3 3 0 1 0-6 0m-6.3-7.3l6.6-3.4m-6.6 6l6.6 3.4"/></svg>

   </div>
   </div>
        
   
</template>

<script setup>

const myImge = new URL("@/assets/MyImge.webp", import.meta.url).href
</script>
<style scope>

.avatar{
  display: flex;
  justify-content: center;
  align-items: start;
  

}
.img{
  height: 100px;
  width: 100px;
  border-radius: 50%;
  margin:  20px 0;
  overflow: hidden;
  border: 2px solid var(--secondary-700);
  background-color: var(--secondary-800);
}
.icon svg{
  width: 25px;
  margin:10px 0;
}
.img img{
  width: 100%;
}
</style>