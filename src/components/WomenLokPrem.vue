<template>
  <div>
    <section class="women-banner spad">
      <div class="container-fluid">
        <div class="row">
          <div class="col-lg-3">
            <div class="product-large set-bg" style="background-image: url('/img/products/women-large.png')">
              <h2>Women’s</h2>
              <a href="#">Discover More</a>
            </div>
          </div>
          <div class="col-lg-8 offset-lg-1">
            <div class="filter-control">
              <ul>
                <li class="active">Complete</li>
                <li>HandBag</li>
                <li>Shoes</li>
              </ul>
            </div>
            <template v-if="products.length > 0">
            <carousel class="product-slider" :items="3" :autoplay="true" :nav="false" :dots="false">
              <div class="product-item" v-for="itemProduct in products" v-bind:key="itemProduct.id">
                <div class="pi-pic">
                  <img v-bind:src="itemProduct.galleries[0].photo"/>
                  <div class="sale">Sale</div>
                  <div class="icon">
                    <i class="icon_heart_alt"></i>
                  </div>
                  <ul>
                    <li class="w-icon active" @click="saveKeranjang(itemProduct.id, itemProduct.name, itemProduct.price, itemProduct.galleries[0].photo)">
                      <a href="#"><i class="icon_bag_alt"></i></a>
                    </li>
                    <li class="quick-view">
                      <router-link v-bind:to="'/product/'+itemProduct.id">+ Quick View</router-link>
                    </li>
                    <li class="w-icon">
                      <a href="#"><i class="fa fa-random"></i></a>
                    </li>
                  </ul>
                </div>
                <div class="pi-text">
                  <div class="catagory-name">{{ itemProduct.type }}</div>
                  <router-link to="/product">
                    <a href="#">
                      <h5>{{ itemProduct.name }}</h5>
                    </a>
                  </router-link>
                  <div class="product-price">
                    ${{ itemProduct.price }}
                    <span>$35.00</span>
                  </div>
                </div>
              </div>
            </carousel>
            </template>
            <template v-else>
              <div class="col-lg-12">
                <p>Produk terbaru belum tersedia untuk saat ini.</p>
              </div>
            </template>
          </div>
        </div>
      </div>
    </section>
    <!-- Women Banner Section End -->
  </div>
</template>

<script>
import carousel from 'vue-owl-carousel';
import axios from "axios";

export default {
  name: 'WomenLokPrem',
  components: {
    carousel,
  },
  data() {
    return {
      products: [],
      keranjangUser: []
    };
  },
  mounted() {
    axios
      .get("http://shayna-backend.belajarkoding.com/api/products")
      .then(response => {
        const {data} = response;
        this.products = data.data.data
      })
      .catch(err => console.log(err));
  },
  methods: {
    saveKeranjang(idProduct, nameProduct, priceProduct, photoProduct) {
      var productStored = {
        id: idProduct,
        name: nameProduct,
        price: priceProduct,
        photo: photoProduct
      };
      this.keranjangUser.push(productStored);
      const parsed = JSON.stringify(this.keranjangUser);
      localStorage.setItem("keranjangUser", parsed);
      window.location.reload()
    }
  }
};
</script>
<style scoped>
.product-item {
  margin-left: 10px;
}
</style>
