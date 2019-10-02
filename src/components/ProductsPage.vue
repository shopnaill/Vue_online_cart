<template>
  <div class="products">
    <ul>
      <li v-bind:key="(js,index)" v-for="(js,index) in myJson">
        <div>

 
            <b-modal :id="'modal-' +index" :title="js.name">
                <div class="row">
                    <div style="padding: 0;" class="col-6">
                       <b-carousel
    id="carousel-fade"
    style="text-shadow: 0px 0px 2px #000"
    fade
    indicators
    img-width="1024"
    img-height="480"
  >
    <b-carousel-slide v-bind:key="photo" v-for="photo in js.photos "
      :img-src="photo"
    ></b-carousel-slide>
   
  </b-carousel>
                    </div>
                    <div class="col-6">
                <p class="my-4">  {{js.description}}</p>

                    </div>
                </div>
            </b-modal>
          <b-card 
            :title="js.name"
            :img-src="js.featuredPhoto"
            img-alt="Image"
            img-top
            tag="article"
            style="max-width: 20rem;"
            class="mb-2"
            v-b-modal="'modal-' +index"
          >
            <font-awesome-icon icon />
              <b-card-text v-if="js.featuredProduct">
                   {{js.description}}
                  </b-card-text>
            <hr />
            <div class="row">
              <div class="col-4">
                <h4>${{js.price}}</h4>
              </div>
              <div class="col-8">
                <b-button href="#" class="btn-sm " style="float: right;" variant="primary sm">ADD TO CART</b-button>
              </div>
            </div>
          </b-card>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
import data from "../assets/db.json";
export default {
  name: "ProductsPage",
  data() {
    return {
      myJson: data.products
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
.carousel-indicators li {
    background-color: #000!important;
    padding: 2px;
}
.card-img-top {
  height: 250px;
}
ol#carousel-fade___BV_indicators_ {
    bottom: -30px;
}
.full-h
{
    height: 325px;
}
h4.card-title {
    font-size: 19px;
    font-weight: bold;
}
</style>
