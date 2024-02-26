<template>
  <router-view/>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');

:root {
  --primary-bg: #0C0C0C;
  --secondary-bg: #111111;
  --primary-text-gradient: linear-gradient(90deg, rgba(0,255,133,1) 0%, rgba(0,255,194,1) 100%);
  --secondary-text-gradient: linear-gradient(90deg, #848484 0%, #B2B2B2 100%);
  --primary-border-gradient: radial-gradient(circle at 100% 100%, #0C0C0C 0, #0C0C0C 6px, transparent 6px) 0% 0%/8px 8px no-repeat,
            radial-gradient(circle at 0 100%, #0C0C0C 0, #0C0C0C 6px, transparent 6px) 100% 0%/8px 8px no-repeat,
            radial-gradient(circle at 100% 0, #0C0C0C 0, #0C0C0C 6px, transparent 6px) 0% 100%/8px 8px no-repeat,
            radial-gradient(circle at 0 0, #0C0C0C 0, #0C0C0C 6px, transparent 6px) 100% 100%/8px 8px no-repeat,
            linear-gradient(#0C0C0C, #0C0C0C) 50% 50%/calc(100% - 4px) calc(100% - 16px) no-repeat,
            linear-gradient(#0C0C0C, #0C0C0C) 50% 50%/calc(100% - 16px) calc(100% - 4px) no-repeat,
            linear-gradient(90deg, rgba(0,255,133,1) 0%, rgba(0,255,194,1) 100%);
  --secondary-border-gradient: radial-gradient(circle at 100% 100%, #0C0C0C 0, #0C0C0C 6px, transparent 6px) 0% 0%/8px 8px no-repeat,
            radial-gradient(circle at 0 100%, #0C0C0C 0, #0C0C0C 6px, transparent 6px) 100% 0%/8px 8px no-repeat,
            radial-gradient(circle at 100% 0, #0C0C0C 0, #0C0C0C 6px, transparent 6px) 0% 100%/8px 8px no-repeat,
            radial-gradient(circle at 0 0, #0C0C0C 0, #0C0C0C 6px, transparent 6px) 100% 100%/8px 8px no-repeat,
            linear-gradient(#0C0C0C, #0C0C0C) 50% 50%/calc(100% - 4px) calc(100% - 16px) no-repeat,
            linear-gradient(#0C0C0C, #0C0C0C) 50% 50%/calc(100% - 16px) calc(100% - 4px) no-repeat,
            linear-gradient(90deg, #848484 0%, #b2b2b2 100%);
  --color-white: #FFF;
  --color-gray: #C4C4C4;
  --color-dark: #0C0C0C;
}

#app {
  width: 100%;
  height: 100vh;
  background-color: var(--primary-bg);
  padding: 0px 50px;
}

* {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  font-family: 'Montserrat';
}

a {
  text-decoration: none;
}

.container {
  max-width: 1380px;
  margin: 0 auto;
}

@media screen and (max-width:640px) {
  #app {
    padding: 0px 10px;
  }
}
</style>
