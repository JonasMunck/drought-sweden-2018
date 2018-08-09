<template>
  <main>
    <section class="section">
      <h1 class="title has-text-centered">Torkan över Sverige</h1>
      <div class="container">
        <div class="columns">
          <div class="column is-half is-offset-one-quarter">
            <p class="subtitle has-text-centered">Foton och inspiration från <a href="https://www.rymdstyrelsen.se/nyheter/2018/sa-ser-sverige-ut-efter-torkan/">Rymdstyrelsen</a></p>
            <p class="subtitle has-text-centered">Skapad 9/8 2018 av <a href="https://github.com/jonasmunck">Jonas Munck af Rosenschöld</a></p>
            <p class="small has-text-centered">Tack till Vue, Nuxt, <a href="https://github.com/marcincichocki">Marcin Cichocki</a></p>
          </div>
        </div>
      </div>
    </section>

    <div v-for="(image, index) in images" :key="index">
      <section class="section" >
        <h1 class="title has-text-centered">{{ image.description }}</h1>
      </section>
      <div class="hero is-fullheight">
        <image-compare :before="image.before" :after="image.after" :full="true"/>
      </div>
      <section class="section" >
        <i>Foto: Rymdstyrelsen/Google/Esa</i>
      </section>

    </div>
  </main>
</template>

<script>


export default {

  data () {
    return {
      images: [
        {
          before: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/blekinge2017_fotorymdstyrelsengoogleesa.jpg',
          after: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/blekinge2018_fotorymdstyrelsengoogleesa.jpg',
          description: 'Satellitbild över Blekinge'
        },
        {
          before: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/gotland2017_fotorymdstyrelsengoogleesa.jpg',
          after: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/gotland2018_fotorymdstyrelsengoogleesa.jpg',
          description: 'Satellitbild över Gotland'
        },
        {
          before: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/jonkoping2017_fotorymdstyrelsengoogleesa.jpg',
          after: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/jonkoping2018_fotorymdstyrelsengoogleesa.jpg',
          description: 'Satellitbild över Jönköping'
        },
        {
          before: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/orebro2017_fotorymdstyrelsengoogleesa.jpg',
          after: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/orebro2018_fotorymdstyrelsengoogleesa.jpg',
          description: 'Satellitbild över Örebro'
        },
        {
          before: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/ostergotland2017_fotorymdstyrelsengoogleesa.jpg',
          after: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/ostergotland2018_fotorymdstyrelsengoogleesa.jpg',
          description: 'Satellitbild över Östergötland'
        },
        {
          before: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/skane2017_fotorymdstyrelsengoogleesa.jpg',
          after: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/skane2018_fotorymdstyrelsengoogleesa.jpg',
          description: 'Satellitbild över Skåne'
        },
        {
          before: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/smaland2017_fotorymdstyrelsengoogleesa.jpg',
          after: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/smaland2018_fotorymdstyrelsengoogleesa.jpg',
          description: 'Satellitbild över Småland'
        },

        {
          before: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/stockholm2017_fotorymdstyrelsengoogleesa.jpg',
          after: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/stockholm2018_fotorymdstyrelsengoogleesa.jpg',
          description: 'Satellitbild över Stockholm'
        },
        {
          before: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/umea2017_fotorymdstyrelsengoogleesa.jpg',
          after: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/umea2018_fotorymdstyrelsengoogleesa.jpg',
          description: 'Satellitbild över Umeå'
        },
        {
          before: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/uppsala2017_fotorymdstyrelsengoogleesa.jpg',
          after: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/uppsala2018_fotorymdstyrelsengoogleesa.jpg',
          description: 'Satellitbild över Uppsala'
        },
        {
          before: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/varmland2017_fotorymdstyrelsengoogleesa.jpg',
          after: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/varmland2018_fotorymdstyrelsengoogleesa.jpg',
          description: 'Satellitbild över Värmland'
        },
        {
          before: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/vastragotaland2017_fotorymdstyrelsengoogleesa.jpg',
          after: 'https://www.rymdstyrelsen.se/contentassets/9f65a925be9c4b2098469a622d9302cd/vastragotaland2018_fotorymdstyrelsengoogleesa.jpg',
          description: 'Satellitbild över Västra Götaland'
        },

      ]
    }
  }

}
</script>

<style>

</style>

