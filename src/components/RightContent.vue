<template>
  <div class="margin-between-container">
    <h4>My Order</h4>

    <div class="order-container">
      <div class="col-12 row" style="padding: 20px;">
        <div class="col-8">
          <p>
            625 St Marks Ave
          </p>
          <b-icon icon="clock" style="color: yellow; "></b-icon>
          <span style="padding-left: 20px">35 min</span>
        </div>
        <div class="col-4" style="color: yellow; text-align: right; padding-right: 0px;">
          <p>
            Edit
          </p>
          <p>
            Choose time
          </p>
        </div>
      </div>
    </div>


    <!--Order Detail-->
    <div class="margin-between-container">
      <div class="order-detail-container">
        <div class="col-12 row">
          <div class="col-4">
            <img class="order-detail-image" src="/images/burger.jpg" />
          </div>
          <div class="col-4 order-detail-text">
            <p>
              1 x Beach BBQBurger
            </p>
          </div>
          <div class="col-4 order-detail-text" style="text-align: right; padding-right: 0px;">
            <p>
              $14.99
            </p>
          </div>
        </div>

        <div class="col-12 row">
          <div class="col-4">
            <img class="order-detail-image" src="/images/frenchfries.jpg" />
          </div>
          <div class="col-4 order-detail-text">
            <p>
              1 x French Fries
            </p>
          </div>
          <div class="col-4 order-detail-text" style="text-align: right; padding-right: 0px;">
            <p>
              $9.99
            </p>
          </div>
        </div>

        <div class="col-12 row">
          <div class="col-4">
            <img class="order-detail-image" src="/images/cheesecake.jpg" />
          </div>
          <div class="col-4 order-detail-text">
            <p>
              1 x Cheese Sause
            </p>
          </div>
          <div class="col-4 order-detail-text" style="text-align: right; padding-right: 0px;">
            <p>
              $0.99
            </p>
          </div>
        </div>

        <div class="col-12 row">
          <div class="col-4">
            <div class="order-detail-delivery-icon">
              <div style="text-align: center; padding-top: 5px;">
                <i class="fas fa-motorcycle"></i>
              </div>
            </div>
          </div>
          <div class="col-4 order-detail-text">
            <p>
              Delivery
            </p>
          </div>
          <div class="col-4 order-detail-text" style="text-align: right; padding-right: 0px;">
            <p>
              $0.00
            </p>
          </div>
        </div>
      </div>
    </div>

    <!--Total Order-->
    <div class="margin-between-container">
      <div class="col-12 row">
        <div class="col-6 total-order-text">
          <p>
            Total:
          </p>
        </div>
        <div class="col-6 total-order-text" style="text-align: right; padding-right: 0px;">
          <p>
            $25.97
          </p>
        </div>
      </div>
    </div>

    <!--Separator line-->
    <div class="separator"></div>

    <!--Input persons and checkout button-->
    <div>
      <div class="col-12 row">
        <div class="col-6 label-persons-text">
          <p>
            Persons
          </p>
          <div style="width: 80%">
            <b-input-group>
              <b-input-group-prepend>
                <b-btn variant="outline-secondary" @click="num--">-</b-btn>
              </b-input-group-prepend>

              <b-form-input type="number" min="0.00" v-model="num"></b-form-input>

              <b-input-group-append>
                <b-btn variant="outline-secondary" @click="num++">+</b-btn>
              </b-input-group-append>
            </b-input-group>
          </div>
        </div>
        <div class="col-6" style="text-align: right;">
          <b-button class="btn-checkout">
            Checkout
            <b-icon icon="arrow-right" aria-hidden="true"></b-icon>
          </b-button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "right-content",
  components: {},
  data() {
    return {
      num: 1,
    };
  },
  methods: {},
};
</script>
