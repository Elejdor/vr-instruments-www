<template>
  <div class="home">
    <section>
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-12 text-center">
            <hr />
            <h1 class="text-uppercase text-secondary">{{ content.idea }}</h1>
            <p>
              {{ content.intro }}
            </p>
          </div>
        </div>

        <div class="col-lg-12">
          <div class="ratio ratio-16x9">
            <iframe
              src="https://www.youtube.com/embed/f26FCFcvOfI"
              alt="https://i.ytimg.com/vi/f26FCFcvOfI/hqdefault.jpg"
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write;
                encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </div>
        </div>

        <div class="row justify-content-center">
          <div class="col-lg-12"></div>
        </div>

        <div>
          <div>
            <hr />
          </div>
        </div>
        <div class="row">
          <div class="col-lg-4">
            <h1 class="text-uppercase text-secondary">{{ content.drumH }}</h1>
            <p>
              {{ content.drum1 }}
            </p>

            <p>
              {{ content.drum2 }}
            </p>
          </div>
          <div class="col-lg-8">
            <video autoplay loop muted>
              <source src="../assets/preview_drum.mp4" type="video/mp4" />
            </video>
          </div>
          <div class="col-lg-12">
            <div class="ratio ratio-16x9">
              <iframe
                src="https://www.youtube.com/embed/_13jrquWZSM"
                title="YouTube video player"
                frameborder="0"
                allow="accelerometer; autoplay; clipboard-write;
              encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-lg-7">
            <h1 class="text-uppercase text-secondary">{{ content.bassH }}</h1>
            <p>
              {{ content.bass }}
            </p>
            <video autoplay loop muted>
              <source src="../assets/preview_bas.mp4" type="video/mp4" />
            </video>
          </div>

          <div class="col-lg-5">
            <img src="../assets/basy-picture.png" class="img-fluid" />
          </div>
        </div>
        <div class="row">
          <div class="col-lg-12">
            <a class="btn btn-primary me-2" href="https://github.com/bebnista-pl/vrInstruments">
              {{ content.source_link }}
            </a>
            <a class="btn btn-primary" href="">
              {{ content.article }}
            </a>
          </div>
        </div>
      </div>
    </section>
    <footer>
      <div class="container">
        <div class="row text-center">
          <div class="col-lg-12">
            <img src="../assets/mkidn_color.jpg" />
            <p>{{ content.footer }}</p>
          </div>
        </div>
      </div>
    </footer>
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue';
import contentPL from '@/assets/content-pl.json';
import contentEn from '@/assets/content-en.json';

export default {
  name: 'Home',
  components: {},
  data() {
    return {
      content: contentPL,
    };
  },
  mounted() {
    const { lang } = this.$route.query;
    console.log(lang);
    if (lang === 'en') {
      this.$data.content = contentEn;
    }
  },
};
</script>
<style scoped>
footer {
  display: block;
}

video {
  width: 100%;
}

.gh-logo {
  width: 100px;
}
</style>
