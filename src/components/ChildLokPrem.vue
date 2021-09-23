<template>
  <div>
    <section class="women-banner spad">
      <div class="container-fluid">
        <div class="row">
          <div class="col-lg-3">
            <div class="product-large set-bg" style="background-image: url('/img/products/child-large.png')">
              <h2>Child's</h2>
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
            <carousel class="product-slider" :items="3" :autoplay="true" :nav="false" :dots="false">
              <div class="product-item">
                <div class="pi-pic">
                  <img src="img/products/child-1.png" />
                  <div class="sale">Sale</div>
                  <div class="icon">
                    <i class="icon_heart_alt"></i>
                  </div>
                  <ul>
                    <li class="w-icon active">
                      <a href="#"><i class="icon_bag_alt"></i></a>
                    </li>
                    <li class="quick-view"><router-link to="/product">+ Quick View</router-link></li>
                    <li class="w-icon">
                      <a href="#"><i class="fa fa-random"></i></a>
                    </li>
                  </ul>
                </div>
                <div class="pi-text">
                  <div class="catagory-name">T-Shirt</div>
                  <a href="#">
                    <h5>Pure Pineapple</h5>
                  </a>
                  <div class="product-price">
                    $14.00
                    <span>$35.00</span>
                  </div>
                </div>
              </div>
              <div class="product-item">
                <div class="pi-pic">
                  <img src="img/products/child-2.png" alt="" />
                  <div class="icon">
                    <i class="icon_heart_alt"></i>
                  </div>
                  <ul>
                    <li class="w-icon active">
                      <a href="#"><i class="icon_bag_alt"></i></a>
                    </li>
                    <li class="quick-view"><router-link to="/product">+ Quick View</router-link></li>
                    <li class="w-icon">
                      <a href="#"><i class="fa fa-random"></i></a>
                    </li>
                  </ul>
                </div>
                <div class="pi-text">
                  <div class="catagory-name">Dress</div>
                  <a href="#">
                    <h5>Guangzhou sweater</h5>
                  </a>
                  <div class="product-price">$13.00</div>
                </div>
              </div>
              <div class="product-item">
                <div class="pi-pic">
                  <img src="img/products/child-3.png" alt="" />
                  <div class="icon">
                    <i class="icon_heart_alt"></i>
                  </div>
                  <ul>
                    <li class="w-icon active">
                      <a href="#"><i class="icon_bag_alt"></i></a>
                    </li>
                    <li class="quick-view"><router-link to="/product">+ Quick View</router-link></li>
                    <li class="w-icon">
                      <a href="#"><i class="fa fa-random"></i></a>
                    </li>
                  </ul>
                </div>
                <div class="pi-text">
                  <div class="catagory-name">Kaca Mata</div>
                  <a href="#">
                    <h5>Pure Pineapple</h5>
                  </a>
                  <div class="product-price">$34.00</div>
                </div>
              </div>
              <div class="product-item">
                <div class="pi-pic">
                  <img src="img/products/child-4.png" alt="" />
                  <div class="icon">
                    <i class="icon_heart_alt"></i>
                  </div>
                  <ul>
                    <li class="w-icon active">
                      <a href="#"><i class="icon_bag_alt"></i></a>
                    </li>
                    <li class="quick-view"><router-link to="/product">+ Quick View</router-link></li>
                    <li class="w-icon">
                      <a href="#"><i class="fa fa-random"></i></a>
                    </li>
                  </ul>
                </div>
                <div class="pi-text">
                  <div class="catagory-name">Rock</div>
                  <a href="#">
                    <h5>Converse Shoes</h5>
                  </a>
                  <div class="product-price">$34.00</div>
                </div>
              </div>
            </carousel>
          </div>
        </div>
      </div>
    </section>
    <!-- Women Banner Section End -->
  </div>
</template>

<script>
import carousel from 'vue-owl-carousel';

export default {
  name: 'ChildLokPrem',
  components: {
    carousel,
  },
};
</script>
<style scoped>
.product-item {
  margin-left: 10px;
}
</style>
