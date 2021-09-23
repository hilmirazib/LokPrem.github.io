<template>
  <div class="product">
    <HeaderLokPrem />
    <BreadLokPrem />
    <ProductShopLokPrem />
    <RelatedLokPrem />
    <PartnerLokPrem />
    <FooterLokPrem />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue';
import HeaderLokPrem from '@/components/HeaderLokPrem.vue';
import FooterLokPrem from '@/components/FooterLokPrem.vue';
import BreadLokPrem from '@/components/BreadLokPrem.vue';
import ProductShopLokPrem from '@/components/ProductShopLokPrem.vue';
import RelatedLokPrem from '@/components/RelatedLokPrem.vue';
import PartnerLokPrem from '@/components/PartnerLokPrem.vue';

export default {
  name: 'Product',
  components: {
    // HelloWorld,
    HeaderLokPrem,
    BreadLokPrem,
    ProductShopLokPrem,
    FooterLokPrem,
    RelatedLokPrem,
    PartnerLokPrem,
  },
};
</script>
