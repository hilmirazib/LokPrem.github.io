<template>
  <div class="home">
    <HeaderLokPrem />
    <HeroLokPrem />
    <BannerLokPrem />
    <WomenLokPrem />
    <ManLokPrem />
    <ChildLokPrem />
    <InstaLokPrem />
    <PartnerLokPrem />
    <FooterLokPrem />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue';
import HeaderLokPrem from '@/components/HeaderLokPrem.vue';
import HeroLokPrem from '@/components/HeroLokPrem.vue';
import BannerLokPrem from '@/components/BannerLokPrem.vue';
import WomenLokPrem from '@/components/WomenLokPrem.vue';
import ManLokPrem from '@/components/ManLokPrem.vue';
import ChildLokPrem from '@/components/ChildLokPrem.vue';
import InstaLokPrem from '@/components/InstaLokPrem.vue';
import PartnerLokPrem from '@/components/PartnerLokPrem.vue';
import FooterLokPrem from '@/components/FooterLokPrem.vue';

export default {
  name: 'Home',
  components: {
    // HelloWorld,
    HeaderLokPrem,
    HeroLokPrem,
    BannerLokPrem,
    WomenLokPrem,
    ManLokPrem,
    ChildLokPrem,
    InstaLokPrem,
    PartnerLokPrem,
    FooterLokPrem,
  },
};
</script>
