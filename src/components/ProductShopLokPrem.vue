<template>
  <div>
    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
      <div class="container">
        <div class="row">
          <div class="col-lg-2">
            <div class="filter-widget text-left">
              <h4 class="fw-title">Categories</h4>
              <ul class="filter-catagories">
                <li><a href="#">Men</a></li>
                <li><a href="#">Women</a></li>
                <li><a href="#">Kids</a></li>
              </ul>
            </div>
          </div>
          <div class="col-lg-10">
            <div class="row">
              <div class="col-lg-6">
                <div class="product-pic-zoom">
                  <img class="product-big-img" :src="gambar_default" alt="" />
                  <div class="zoom-icon">
                    <i class="fa fa-search-plus"></i>
                  </div>
                </div>
                <div class="product-thumbs" v-if="productDetails.galleries.length > 0">
                  <carousel class="product-thumbs-track ps-slider" :items="3" :autoplay="true" :nav="false" :dots="false">
                    <!-- <div class="pt active" @click="changeImage(thumbs[0])" :class="thumbs[0] == gambar_default ? 'active' : ''">
                      <img src="img/product-single/product-1.png" alt="" />
                    </div> -->
                    <div
                      v-for="item in productDetails.galleries"
                      :key="item.id"
                      class="pt"
                      @click="changeImage(item.photo)"
                      :class="item.photo == gambar_default ? 'active' : '' "
                    >
                      <img :src="item.photo" alt />
                    </div>
                  </carousel>
                </div>
              </div>
              <div class="col-lg-6">
                <div class="product-details text-left">
                  <div class="pd-title text-left">
                    <span>{{ productDetails.type }}</span>
                    <h3>{{ productDetails.name }}</h3>
                    <a href="#" class="heart-icon"><i class="icon_heart_alt"></i></a>
                  </div>

                  <div class="pd-desc">
                    <p v-html="productDetails.description"></p>
                    <h4>${{ productDetails.price }}</h4>
                  </div>
                  <!-- <div class="pd-color">
                    <h6>Color</h6>
                    <div class="pd-color-choose">
                      <div class="cc-item">
                        <input type="radio" id="cc-black" />
                        <label for="cc-black"></label>
                      </div>
                      <div class="cc-item">
                        <input type="radio" id="cc-yellow" />
                        <label for="cc-yellow" class="cc-yellow"></label>
                      </div>
                      <div class="cc-item">
                        <input type="radio" id="cc-violet" />
                        <label for="cc-violet" class="cc-violet"></label>
                      </div>
                    </div>
                  </div>
                  <div class="pd-size-choose">
                    <div class="sc-item">
                      <input type="radio" id="sm-size" />
                      <label for="sm-size">s</label>
                    </div>
                    <div class="sc-item">
                      <input type="radio" id="md-size" />
                      <label for="md-size">m</label>
                    </div>
                    <div class="sc-item">
                      <input type="radio" id="lg-size" />
                      <label for="lg-size">l</label>
                    </div>
                    <div class="sc-item">
                      <input type="radio" id="xl-size" />
                      <label for="xl-size">xs</label>
                    </div>
                  </div> -->
                  <div class="quantity">
                    <router-link to="/product/shoppingCart"><a @click="saveKeranjang(productDetails.id, productDetails.name, productDetails.price, productDetails.galleries[0].photo)" href="#" class="primary-btn pd-cart">Add To Cart</a></router-link>
                  </div>
                </div>
              </div>
            </div>
            <div class="product-tab">
              <div class="tab-item">
                <ul class="nav" role="tablist">
                  <li>
                    <a class="active" data-toggle="tab" href="#tab-1" role="tab">DESCRIPTION</a>
                  </li>
                  <li>
                    <a data-toggle="tab" href="#tab-2" role="tab">SPECIFICATIONS</a>
                  </li>
                  <li>
                    <a data-toggle="tab" href="#tab-3" role="tab">Customer Reviews (02)</a>
                  </li>
                </ul>
              </div>
              <div class="tab-item-content">
                <div class="tab-content">
                  <div class="tab-pane fade-in active" id="tab-1" role="tabpanel">
                    <div class="product-content">
                      <div class="row">
                        <div class="col-lg-7 text-left">
                          <h5>Introduction</h5>
                          <p>
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna
                            aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis
                            aute irure dolor in
                          </p>
                          <h5>Features</h5>
                          <p>
                            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna
                            aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis
                            aute irure dolor in
                          </p>
                        </div>
                        <div class="col-lg-5">
                          <img src="img/product-single/tab-desc.png" alt="" />
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="tab-pane fade" id="tab-2" role="tabpanel">
                    <div class="specification-table">
                      <table>
                        <tr>
                          <td class="p-catagory">Customer Rating</td>
                          <td>
                            <div class="pd-rating">
                              <i class="fa fa-star"></i>
                              <i class="fa fa-star"></i>
                              <i class="fa fa-star"></i>
                              <i class="fa fa-star"></i>
                              <i class="fa fa-star-o"></i>
                              <span>(5)</span>
                            </div>
                          </td>
                        </tr>
                        <tr>
                          <td class="p-catagory">Price</td>
                          <td>
                            <div class="p-price">$495.00</div>
                          </td>
                        </tr>
                        <tr>
                          <td class="p-catagory">Add To Cart</td>
                          <td>
                            <div class="cart-add">+ add to cart</div>
                          </td>
                        </tr>
                        <tr>
                          <td class="p-catagory">Availability</td>
                          <td>
                            <div class="p-stock">22 in stock</div>
                          </td>
                        </tr>
                        <tr>
                          <td class="p-catagory">Weight</td>
                          <td>
                            <div class="p-weight">1,3kg</div>
                          </td>
                        </tr>
                        <tr>
                          <td class="p-catagory">Size</td>
                          <td>
                            <div class="p-size">Xxl</div>
                          </td>
                        </tr>
                        <tr>
                          <td class="p-catagory">Color</td>
                          <td><span class="cs-color"></span></td>
                        </tr>
                        <tr>
                          <td class="p-catagory">Sku</td>
                          <td>
                            <div class="p-code">00012</div>
                          </td>
                        </tr>
                      </table>
                    </div>
                  </div>
                  <div class="tab-pane fade" id="tab-3" role="tabpanel">
                    <div class="customer-review-option">
                      <h4>2 Comments</h4>
                      <div class="comment-option">
                        <div class="co-item">
                          <div class="avatar-pic">
                            <img src="img/product-single/avatar-1.png" alt="" />
                          </div>
                          <div class="avatar-text">
                            <div class="at-rating">
                              <i class="fa fa-star"></i>
                              <i class="fa fa-star"></i>
                              <i class="fa fa-star"></i>
                              <i class="fa fa-star"></i>
                              <i class="fa fa-star-o"></i>
                            </div>
                            <h5>Brandon Kelley <span>27 Aug 2019</span></h5>
                            <div class="at-reply">Nice !</div>
                          </div>
                        </div>
                        <div class="co-item">
                          <div class="avatar-pic">
                            <img src="img/product-single/avatar-2.png" alt="" />
                          </div>
                          <div class="avatar-text">
                            <div class="at-rating">
                              <i class="fa fa-star"></i>
                              <i class="fa fa-star"></i>
                              <i class="fa fa-star"></i>
                              <i class="fa fa-star"></i>
                              <i class="fa fa-star-o"></i>
                            </div>
                            <h5>Roy Banks <span>27 Aug 2019</span></h5>
                            <div class="at-reply">Nice !</div>
                          </div>
                        </div>
                      </div>
                      <div class="personal-rating">
                        <h6>Your Ratind</h6>
                        <div class="rating">
                          <i class="fa fa-star"></i>
                          <i class="fa fa-star"></i>
                          <i class="fa fa-star"></i>
                          <i class="fa fa-star"></i>
                          <i class="fa fa-star-o"></i>
                        </div>
                      </div>
                      <div class="leave-comment">
                        <h4>Leave A Comment</h4>
                        <form action="#" class="comment-form">
                          <div class="row">
                            <div class="col-lg-6">
                              <input type="text" placeholder="Name" />
                            </div>
                            <div class="col-lg-6">
                              <input type="text" placeholder="Email" />
                            </div>
                            <div class="col-lg-12">
                              <textarea placeholder="Messages"></textarea>
                              <button type="submit" class="site-btn">Send message</button>
                            </div>
                          </div>
                        </form>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Product Shop Section End -->
  </div>
</template>

<script>
import carousel from 'vue-owl-carousel';
import axios from "axios";
export default {
  name: 'ProductShopLokPrem',
  components: {
    carousel,
  },
  // data() {
  //   return {
  //     gambar_default: 'img/product-single/product-1.png',
  //     thumbs: [
  //       'img/product-single/product-1.png',
  //       'img/product-single/product-2.png',
  //       'img/product-single/product-3.png',
  //       'img/product-single/product-3.png',
  //     ],
  //     default_photo: '',
  //   };
  // },
  data() {
    return {
      gambar_default: "",
      productDetails: [],
      keranjangUser: []
    };
  },
  
  methods: {
    changeImage(urlImage) {
      this.gambar_default = urlImage;
    },
    setDataPicture(data) {
      this.productDetails = data;
      this.gambar_default = data.galleries[0].photo;
    },
    saveKeranjang(idProduct, nameProduct, priceProduct, photoProduct) {

      var productStored = {
        "id": idProduct,
        "name": nameProduct,
        "price": priceProduct,
        "photo": photoProduct
      }

      this.keranjangUser.push(productStored);
      const parsed = JSON.stringify(this.keranjangUser);
      localStorage.setItem('keranjangUser', parsed);
    }
  },
  mounted() {
    if (localStorage.getItem('keranjangUser')) {
      try {
        this.keranjangUser = JSON.parse(localStorage.getItem('keranjangUser'));
      } catch(e) {
        localStorage.removeItem('keranjangUser');
      }
    }
    axios
      .get("http://shayna-backend.belajarkoding.com/api/products", {
        params: {
          id: this.$route.params.id
        }
      })
      .then(res => this.setDataPicture(res.data.data))
      // eslint-disable-next-line no-console
      .catch(err => console.log(err));
  }
};
</script>
<style scoped>
.product-thumbs .pt {
  margin-right: 10px;
}
</style>
