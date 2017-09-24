<template>
<!-- The individual cards. Will be rendered dynamically. -->
  <div class="container">
    <div class="row">
      <!-- the text above the cards. -->
      <div class="col-12 col-md-6 mx-auto text-center mb-5">
        {{ paragraph }}
      </div> 
      <!-- text end -->
    </div>
    <div class="row justify-content-center mt-3">
      <!-- each card -->
      <div class="col-12 col-md-6 col-xl-3 align-self-center" v-for="(card, index) in cards" :key="index">
        <div class="card text-center bg-gray mb-5 not-rounded has-shadow">
          <div class="card-body text-active">
            <!-- check if card is popular. will change class accordingly -->
            <div v-if="card.isPopular" class="h4 text-red text-uppercase mt-2 mb-0">most popular</div>
            <div class="title text-center">{{ card.title }}</div>
            <!-- bigger text for most popular card -->
            <div class="font-weight-bold"
            :class="{'display-3' : !card.isPopular, 'display-2' : card.isPopular}">&euro;{{ card.price}}</div>
            <!-- check if card has savings. will render an empty space if not -->
            <div v-if="card.savings" class="savings small mb-1">Save &euro;{{ card.savings }}</div>
            <!-- check if card has deadline. will render an empty space if not -->
            <div v-else-if="card.deadline" class="savings mb-1">&nbsp;</div>
            <div v-if="card.deadline" class="mb-2">Until {{ card.deadline }}</div>
            <!-- check if card has promo code. will put an input and a selection of dates if yes. -->
            <div v-else class="mb-2">
              <div class="text-muted small">Do you have a promo code?</div>
                <!-- promo code input -->
                <input type="text" class="form-control-sm custom-input my-1" placeholder="Type it here & pick a day">
                <!-- input end -->
                <!-- radio selection input -->
                <ul class="list-unstyled list-inline custom-radio">
                  <li class="list-inline-item">
                    <input id="day1" class="form-check-input" type="radio" name="day" value="option1">
                    <label for="day1" class="form-check-label">DAY 1</label>
                  </li>
                  <li class="list-inline-item">
                    <input id="day2" class="form-check-input" type="radio" name="day" value="option2">
                    <label for="day2" class="form-check-label">DAY 2</label>
                  </li>
                  <li class="list-inline-item">
                    <input id="day3" class="form-check-input" type="radio" name="day" value="option3">
                    <label for="day3" class="form-check-label">BOTH</label>
                  </li>
                </ul>
                <!-- radio selection end -->
            </div>
            <!-- benefits of the card. should be different for each card.
            for this example, the benefits are the same. -->
            <div class="benefits mt-4" v-bind:style="{'height': getHeight}">
              <ul class="text-left">
                <li v-for="(benefit,index) in card.benefits" :key="index">
                  <span class="text-dark text-left">
                    {{ benefit }}
                  </span>
                </li>
              </ul>
            </div>
            <!-- benefits end -->
          </div>
          <!-- book now button. will change color if the card is most popular. -->
          <button class="btn btn-block text-uppercase not-rounded font-weight-bold p-4"
          :class="{'btn-red' : card.isPopular, 'btn-active': !card.isPopular}">
            book now
          </button>
          <!-- button end -->
        </div>
      </div>
      <!-- controller for benefits. clicking will show the benefits and will change text to 'close'.
      clicking again will hide benefits and revert text to original. -->
      <div class="col-12 text-center mb-5">
        <button class="btn btn-active-inverse text-uppercase font-weight-bold not-rounded py-2 px-4" @click="toggleBenefits">
          {{ btnText }}
        </button>
      </div>
      <!-- controller end -->
    </div>
  </div>
</template>

<script>
// array of benefits. can be changed indivually per card. just add this array to the cards object.
let benefits = [
  'Cold-pressed poke thundercats brooklyn chillware chartreuse',
  'Craft beer 3 moon tbh hoodie',
  'YOLO synth hammock',
  'Distillery aesthetic VHS affogato gentrify bespoke',
  'Chia readymade schlitz brunch yuccie echo park'
]
export default {
  name: 'cards',
  data () {
    return {
      // text on of of cards
      paragraph: 'Fashion axe truffaut migas Farm-to-table PBR&B. Drinking vinegar sustainable helvetica sartorial. Dreatmcatcher live-edge lo-fi, chartreuse echo park pinterest distillery glossier plaid fingerstache. Fashion axe keytar truffaut migas Farm-to-table PBR&B. Drinking vinegar sustainable helvetica',
      // text of controller
      btnText: 'compare benefits',
      // benefits not shown at initial page render
      showBenefits: false,
      // individual cards
      cards: [
        {
          isPopular: false,
          title: 'summer saver',
          price: 1595,
          savings: 300,
          deadline: 'August 31',
          benefits: benefits
        },
        {
          isPopular: true,
          title: 'expo only',
          price: 299,
          savings: null,
          deadline: 'October',
          benefits: benefits
        },
        {
          isPopular: false,
          title: 'public & govermental sector',
          price: 1295,
          savings: '300 from the Summer Saver',
          deadline: 'October',
          benefits: benefits
        },
        {
          isPopular: false,
          title: 'standard conference & expo',
          price: 1695,
          savings: null,
          deadline: '',
          benefits: benefits
        }
      ]
    }
  },
  methods: {
    // function for showing and hiding benefits
    toggleBenefits () {
      switch (this.btnText) {
        case 'compare benefits':
          this.showBenefits = true
          this.btnText = 'close'
          break
        case 'close':
          this.showBenefits = false
          this.btnText = 'compare benefits'
          break
      }
    }
  },
  // for the animation of benefits when shown and hidden.
  computed: {
    getHeight () {
      return this.showBenefits ? '13rem' : '0px'
    }
  }
}
</script>
