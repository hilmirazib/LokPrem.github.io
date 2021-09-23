<template>
  <div>
    <!-- Hero Section Begin -->
    <section class="hero-section">
      <carousel class="hero-items" :items="1" :autoplay="true" :nav="false" :dots="false">
        <div class="single-hero-items set-bg" style="background-image: url('/img/hero1.png')">
          <div class="container">
            <div class="row">
              <div class="col-lg-5">
                <span>T-Shirt Premium</span>
                <h1>T-Shirt Polos Premium Weight</h1>
                <p>
                  Kami bekerja dalam berbagai program pemantauan untuk menjamin kepatuhan terhadap standar keselamatan, kesehatan, dan kualitas setiap
                  produk kami.
                </p>
                <a href="#" class="shop-now btn-lg text-white">Shop Now</a>
              </div>
            </div>
            <div class="off-card">
              <h2>Sale <span>50%</span></h2>
            </div>
          </div>
        </div>
        <div class="single-hero-items set-bg" style="background-image: url('/img/hero2.png')">
          <div class="container">
            <div class="row">
              <div class="col-lg-5">
                <span>T-Shirt Premium</span>
                <h1>T-Shirt Polos Premium Weight</h1>
                <p>
                  Kami bekerja dalam berbagai program pemantauan untuk menjamin kepatuhan terhadap standar keselamatan, kesehatan, dan kualitas setiap
                  produk kami.
                </p>
                <a href="#" class="shop-now btn-lg text-white">Shop Now</a>
              </div>
            </div>
            <div class="off-card">
              <h2>Sale <span>50%</span></h2>
            </div>
          </div>
        </div>
        <div class="single-hero-items set-bg" style="background-image: url('/img/hero1.png')">
          <div class="container">
            <div class="row">
              <div class="col-lg-5">
                <span>T-Shirt Premium</span>
                <h1>T-Shirt Polos Premium Weight</h1>
                <p>
                  Kami bekerja dalam berbagai program pemantauan untuk menjamin kepatuhan terhadap standar keselamatan, kesehatan, dan kualitas setiap
                  produk kami.
                </p>
                <a href="#" class="shop-now btn-lg text-white">Shop Now</a>
              </div>
            </div>
            <div class="off-card">
              <h2>Sale <span>50%</span></h2>
            </div>
          </div>
        </div>
      </carousel>
    </section>
    <!-- Hero Section End -->
  </div>
</template>

<script>
import carousel from 'vue-owl-carousel';

export default {
  name: 'HeroLokPrem',
  components: {
    carousel,
  },
};
</script>
