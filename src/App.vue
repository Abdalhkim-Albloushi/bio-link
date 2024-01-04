<template>
<div>
  
  <Profile />
</div>
</template>
<script setup>
import Profile from './components/Profile.vue.vue';

</script>
<style>
:root {
  
  --text-50: #e5fff7;
--text-100: #ccfff0;
--text-200: #99ffe0;
--text-300: #66ffd1;
--text-400: #33ffc2;
--text-500: #00ffb3;
--text-600: #00cc8f;
--text-700: #00996b;
--text-800: #006647;
--text-900: #003324;
--text-950: #001a12;

--background-50: #e5fff8;
--background-100: #ccfff1;
--background-200: #99ffe2;
--background-300: #66ffd4;
--background-400: #33ffc5;
--background-500: #00ffb7;
--background-600: #00cc92;
--background-700: #00996e;
--background-800: #006649;
--background-900: #003325;
--background-950: #001a12;

--primary-50: #e6fef9;
--primary-100: #cdfef3;
--primary-200: #9bfde8;
--primary-300: #69fcdc;
--primary-400: #37fbd0;
--primary-500: #05fac5;
--primary-600: #04c89d;
--primary-700: #039676;
--primary-800: #02644f;
--primary-900: #013227;
--primary-950: #011914;

--secondary-50: #e6f6fe;
--secondary-100: #cdecfe;
--secondary-200: #9bd9fd;
--secondary-300: #69c6fc;
--secondary-400: #37b3fb;
--secondary-500: #05a0fa;
--secondary-600: #0480c8;
--secondary-700: #036096;
--secondary-800: #024064;
--secondary-900: #012032;
--secondary-950: #011019;

--accent-50: #e6f1fe;
--accent-100: #cde2fe;
--accent-200: #9bc5fd;
--accent-300: #69a9fc;
--accent-400: #378cfb;
--accent-500: #056ffa;
--accent-600: #0459c8;
--accent-700: #034396;
--accent-800: #022c64;
--accent-900: #011632;
--accent-950: #010b19;


}
@font-face {
  font-family: "EnFont";
  src: url('./assets/fonts/Calibri-Regular.ttf');
}


*{
  padding: 0;
  margin: 0;
}
body{
  background-color: var(--background-50);
  color: var(--text-800);
  margin: 16px;
}
#app {
  font-family: EnFont, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  box-sizing: border-box;
}

/* #9C9C9C */
</style>
