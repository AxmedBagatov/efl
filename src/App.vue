<template>
  <v-app>
    <v-app-bar app elevate  color="rgb(29,29,29)">
      <!-- <div class="d-flex align-center"> -->
        <router-link to="/" style="text-decoration: none;">
          <!-- <v-btn flat color="green accent-3" text rounded class="display-1 font-weight-black" > EFL </v-btn> -->
          <v-img alt="Vuetify Name" max-height="30" max-width="50" contain class="logomain" 
            src="../src/assets/EFL.png" width="100" />
          </router-link> 
      <!-- </div> -->

      <v-spacer></v-spacer>
      <router-link v-for="route in routes" :key="route" :to=" route.path" style="text-decoration: none; color: inherit;">
      <v-btn flat color="green accent-3" text rounded class="my-2">{{ route.name }}</v-btn>
    </router-link>
 
    
    </v-app-bar>

    <v-content class="aboutmain">
      <router-view></router-view>
    </v-content>

  </v-app>

</template>

<script>



export default {
  name: 'App',
  data: () => ({
    routes: [
      {
        path: '/table',
        name: 'Таблица',
      }, {
        path: '/team',
        name: 'Команды',
      }, {
        path: '/players',
        name: 'Игроки',
      }, {
        path: '/matches',
        name: 'Матчи',
      }
    ],
    //
  }),
};
</script>

26.7deg
<style>
.aboutmain {
  padding-inline: 130px;
  min-width: 600px;

  /* background: linear-gradient(207deg,rgba(0, 0, 0, 1) 65%,rgba(1, 51, 5, 1) 0%); */
}

::-webkit-scrollbar{
  width: 20px;
}

::-webkit-scrollbar-track{
  background: #000000;
}

::-webkit-scrollbar-thumb{
  background: #013305;
 /* background: #77ff21; */
}



.logomain{
  width: 15%;
  aspect-ratio: 3/2;
  object-fit: contain;
  mix-blend-mode: color-burn;
}

*, *:after, *:before {
   box-sizing: border-box;
   padding: 0;
   margin: 0;
   transition: .5s ease-in-out;
   /* добавим плавность переходов для всех элементов страницы*/
}
@media screen  {
  
}
</style>

