<template>
  <div class="home">
    <div class="gradient_1">
      <h1 class="mainheader">Эндирейская Футбольная Лига</h1>
      <div class="caru">
        <v-carousel cycle height="400" hide-delimiter-background show-arrows-on-hover>
          <v-carousel-item v-for="(slide, i) in slides" :key="i">
            <v-sheet :color="colors[i]" height="100%">
              <v-row class="fill-height" align="center" justify="center">
                <div class="text-h2">
                  {{ slide }} Slide
                </div>
              </v-row>
            </v-sheet>
          </v-carousel-item>
        </v-carousel>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam accusantium, ab consectetur deserunt quo
          similique consequatur fugit aperiam odio, repudiandae laudantium. Harum enim provident laudantium unde
          similique dignissimos, nulla illo.</p>
      </div>

      <div class="teams">

        <h1>Команды</h1>
        <p style="max-width:700px">Lorem ipsum dolor sit amet consectetur adipisicing elit. Animi culpa reprehenderit,
          ipsam expedita modi temporibus itaque magnam illo eum similique numquam incidunt, molestias eligendi, soluta
          earum voluptatum ad impedit. Nam.</p>
      </div>
      <router-link to="/team" style="text-decoration: none; color: inherit;">
        <v-btn class="green accent-3" width="200px" height="38px" rounded>Перейти к командам</v-btn></router-link>

        <div class="tablHome">

        Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro harum exercitationem obcaecati voluptas dicta magnam? Ipsa accusamus molestias consequatur, eos laborum esse quae odio voluptatem molestiae! Eaque cum laboriosam sequi!

        </div>

    </div>
    <div class="gradient_2">

    </div>
  </div>


</template>

<script>


export default {
  name: 'Home',
  data() {
    return {
      colors: [
        'indigo',
        'warning',
        'pink darken-2',
        'red lighten-1',
        'deep-purple accent-4',
      ],
      slides: [
        'First',
        'Second',
        'Third',
        'Fourth',
        'Fifth',
      ],
    }
  },
}
</script>


<style>
.caru {
  width: 50%;
  margin-block: 60px;
  margin-inline: 40px;
}

.home {
  padding-inline: 50px;
  color: white;
  z-index: 2;
  height: 200vh;
background-color: black;
}

.mainheader {
  padding-block-start: 20px;
}

.gradient_1 {
  background: linear-gradient(30deg, rgba(0, 0, 0, 1) 65%, rgba(1, 51, 5, 1) 0%);
  height: 30%;
  width: 100%;
  position: absolute;
  z-index: 2;
  right: 0;
  top: 0;
}

.gradient_2 {
  background: linear-gradient(207deg, rgba(0, 0, 0, 1) 65%, rgba(1, 51, 5, 1) 0%);

  height: 50%;
  width: 100%;
  z-index: 0;
  position: absolute;
  bottom: 0;
  left: 0;
}
</style>