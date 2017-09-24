<template>
  <div class="container mb-5">
    <!-- for displaying the partners. can be made dynamic using javascript.
    for the purpose of the mockup, each partner will be the same. -->
    <div class="row justify-content-center">
      <div class="col-12 text-center mb-4">
        <div class="text-muted text-uppercase">
          our trusted partners
        </div>
      </div>
      <div class="col-12 text-center">
        <div class="d-inline-block m-4" v-for="(n,index) in 5" :key="index">
          <img class="img-fluid fixed-height" src="./../../static/img/partner.png">
        </div>
      </div>
    </div>
    <!-- partners end -->
  </div>
</template>

<script>
export default {
  name: 'partners'
}
</script>

