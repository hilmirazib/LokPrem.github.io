<template>
  <div>
    <!-- Man Banner Section Begin -->
    <section class="man-banner spad">
      <div class="container-fluid">
        <div class="row">
          <div class="col-lg-8">
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
                  <img src="img/products/man-1.png" alt="" />
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
                  <div class="catagory-name">Coat</div>
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
                  <img src="img/products/man-2.png" alt="" />
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
                  <div class="catagory-name">Shoes</div>
                  <a href="#">
                    <h5>Guangzhou sweater</h5>
                  </a>
                  <div class="product-price">$13.00</div>
                </div>
              </div>
              <div class="product-item">
                <div class="pi-pic">
                  <img src="img/products/man-3.png" alt="" />
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
                  <div class="catagory-name">Towel</div>
                  <a href="#">
                    <h5>Pure Pineapple</h5>
                  </a>
                  <div class="product-price">$34.00</div>
                </div>
              </div>
              <div class="product-item">
                <div class="pi-pic">
                  <img src="img/products/man-4.png" alt="" />
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
                  <div class="catagory-name">Towel</div>
                  <a href="#">
                    <h5>Converse Shoes</h5>
                  </a>
                  <div class="product-price">$34.00</div>
                </div>
              </div>
            </carousel>
          </div>
          <div class="col-lg-3 offset-lg-1">
            <div class="product-large set-bg m-large" style="background-image: url('/img/products/man-large.png')">
              <h2>Men’s</h2>
              <a href="#">Discover More</a>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Man Banner Section End -->
  </div>
</template>

<script>
import carousel from 'vue-owl-carousel';

export default {
  name: 'ManLokPrem',
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
