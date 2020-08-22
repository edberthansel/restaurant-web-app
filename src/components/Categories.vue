<template>
  <div class="margin-between-container">
    <div class="row">
      <div class="col-8">
        <h4>Restaurants</h4>
      </div>
      <div class="col-4" style="text-align: right;">
        <b-button class="btn-delivery-now">
          <b-icon icon="clock" aria-hidden="true"></b-icon>
          Delivery: Now
          <b-icon icon="chevron-down" aria-hidden="true"></b-icon>
        </b-button>
      </div>
    </div>

    <!--Carousel-->
    <div class="margin-between-container">
      <div
        class="owl-carousel owl-theme"
        style="text-align: center; font-size: 30px;"
      >
        <div v-for="(category, index) in categoryList" :key="index">
          <button
            class="btn carousel-items"
            :class="{ active: isActiveItem(category) }"
            @click="changeColour(category)"
          >
            <img :src="category.iconUrl" class="carousel-icons" />
            <p>{{ category.name }}</p>
          </button>
        </div>
      </div>
    </div>

    <!--Cards-->
    <div style="margin-top: 10px !important;">
      <b-card-group deck>
        <b-card
          class="cards-container"
          no-body
          img-src="/images/bagel.jpg"
          img-height="200px"
        >
          <b-card-header class="cards-header-container">
            <div class="col-5 cards-header-text">
              <h6>25-30 min</h6>
            </div>
          </b-card-header>

          <b-card-body>
            <b-card-title>Bagel Story</b-card-title>
            <b-card-text class="cards-text">
              <b-icon icon="star" aria-hidden="true"></b-icon> 4.7 Deli Bagels
              $$
            </b-card-text>
          </b-card-body>
        </b-card>

        <b-card
          class="cards-container"
          no-body
          img-src="/images/pizza.jpg"
          img-height="200px"
        >
          <b-card-header class="cards-header-container">
            <div class="col-5 cards-header-text">
              <h6>30-35 min</h6>
            </div>
          </b-card-header>

          <b-card-body>
            <b-card-title>The Estaminet</b-card-title>
            <b-card-text class="cards-text">
              <b-icon icon="star" aria-hidden="true"></b-icon> 4.5 Cafes
              Creperies $
            </b-card-text>
          </b-card-body>
        </b-card>

        <b-card
          class="cards-container"
          no-body
          img-src="/images/pastry.jpg"
          img-height="200px"
        >
          <b-card-header class="cards-header-container">
            <div class="col-5 cards-header-text">
              <h6>40-60 min</h6>
            </div>
          </b-card-header>

          <b-card-body>
            <b-card-title>Le Paris Dakar</b-card-title>
            <b-card-text class="cards-text">
              <b-icon icon="star" aria-hidden="true"></b-icon> 4.6 Creperies
              Sandwich $$
            </b-card-text>
          </b-card-body>
        </b-card>
      </b-card-group>
    </div>
  </div>
</template>

<script>
export default {
  name: "Categories",
  components: {},
  data() {
    return {
      activeItem: "",
      categoryList: [
        {
          id: 0,
          name: "All",
          iconUrl: "/images/allfood.png",
        },
        {
          id: 1,
          name: "Pizza",
          iconUrl: "/images/pizza-icon.png",
        },
        {
          id: 2,
          name: "Asian",
          iconUrl: "/images/asian-icon.png",
        },
        {
          id: 3,
          name: "Burgers",
          iconUrl: "/images/burger-icon.png",
        },
        {
          id: 4,
          name: "Barbecue",
          iconUrl: "/images/barbecue-icon.png",
        },
        {
          id: 5,
          name: "Desserts",
          iconUrl: "/images/dessert-icon.png",
        },
        {
          id: 6,
          name: "Thai",
          iconUrl: "/images/thai-icon.png",
        },
        {
          id: 7,
          name: "Sushi",
          iconUrl: "/images/sushi-icon.png",
        },
      ],
    };
  },
  methods: {
    changeColour(category) {
      this.activeItem = category;
    },
    isActiveItem(category) {
      return this.activeItem === category;
    },
  },
};
</script>
