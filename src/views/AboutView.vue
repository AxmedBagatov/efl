<template>
    <div class="maincard ">
        <div class="contentcard grey darken-4">
            <h1 class="headermain">Списки команд</h1>
            <!-- <div v-for="team in teams" key="team" color="grey darken-4">
                    <v-img src={{ team.img }}></v-img>
                </div>  -->
            <div class="flexmain"> 
                <div v-for="team in teams" :key="team" class="carddiv">
                    <div class="textmain">
                        <h2 class="white--text" style="padding-block: 5px"> {{ team.name }}</h2>
                        <v-card class="cardmain" :img="require(`@/assets/${team.img}`)" color="grey darken-4">
                            <!-- <v-img class="imagemain" :src="require(`@/assets/${team.img}`)"> -->
                            <!-- </v-img> -->
                            <!-- <v-img src="@/assets/team.png"></v-img> -->
                        </v-card>
                    </div>

                    <!-- <div class="text-center">
                        <v-dialog v-model="dialog" width="500" color="black">
                            <template v-slot:activator="{ on, attrs }">
                                <v-btn color="red lighten-2" dark v-bind="attrs" v-on="on">
                                    Click Me
                                </v-btn>
                            </template>

                            <v-card>
                                <v-card-title class="text-h5 grey lighten-2">
                                    Privacy Policy
                                </v-card-title>

                                <v-card-text>
                                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                                    incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud
                                    exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute
                                    irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
                                    pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia
                                    deserunt mollit anim id est laborum.
                                </v-card-text>
                            </v-card>
                        </v-dialog>
                    </div> -->


                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'About',
    data () {
      return {
        dialog: false,
        teams: [{
            img: 'team.png',
            name: 'Бейрут',
        },
        {
            img: 'birlik.png',
            name: 'Бирлик',
        },
        {
            img: 'turan.png',
            name: 'Туран',
        },
        {
            img: 'ridjal.png',
            name: 'Риджаль',
        },
        {
            img: 'brat.png',
            name: 'Братсво',
        },
        {
            img: 'legion.png',
            name: 'Легион',
        },
        {
            img: 'zavod.png',
            name: 'Завод аул',
        },
        {
            img: 'turan.png',
            name: 'Оьр-аул',
        },
        {
            img: 'soltan.png',
            name: 'Солтан-Мут',
        },
        {
            img: 'beyrut.png',
            name: 'Эндери',
        },
        {
            img: 'ridjal.png',
            name: 'Ханиф',
        },
        ],
    }
},
}
</script>

<style>
.imagemain {
    width: 100%;
    height: 100%;
}

.carddiv {
    margin-inline: 20%;
    text-align: center;
}

.flexmain {
    padding-block-start: 30px;
    margin-inline-start: 4%;
    display: grid;
    /* justify-content: space-around; */
    grid-template-columns: auto auto auto;
    grid-column-gap: 10px;
    grid-row-gap: 3em;
}

/* .contentcard{
    display: flex;
} */

.cardmain {
    width: 100%;
    height: 150px;
}

.headermain {
    text-align: center;
    color: White;
    padding-block-start: 30px;
}

.green {
    width: 100%;
    height: 100%;
    padding-inline: 8%;
}

@media screen and (max-width: 250px) {}

.maincard {
    width: 100%;
    height: 180vh;
    /* padding-inline: 150px; */
    background: repeating-linear-gradient(45deg,
            #000000,
            #061708 10px,
            #013305 10px,
            #013305 20px);
    /* background: #013305; */
    /* background: orange; */
}

.contentcard {
   
    background: repeating-linear-gradient(45deg,
            #00000070,
            #025f0983 2px,
            #042c0557 2px,
            #08040028 2px);
    width: 100%;
    height: 100%;
}
</style>