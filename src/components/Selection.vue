<template>
  <div class="container-fluid bg-gray height-maxed has-shadow">
    <div class="row no-gutters d-flex align-items-center justify-content-center py-3 py-sm-4">
      <div class="col-3 text-center fixed-height" v-for="(selection,index) in selections" :key="index">
        <a class="small-font-sm no-underline" 
           :class="{'is-active' : selection.isActive, 'text-dark' : !selection.isActive}" 
           href="#" 
           @click="toggleActive(index)">
          <i :class="selection.icon" class="fa fa-fw d-block mx-auto d-sm-inline-block"></i>
          <span> {{ selection.name }}</span>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'selection',
  data () {
    return {
      selections: [
        {
          name: 'SINGLE ATTENDEE',
          icon: 'fa-user',
          isActive: true
        },
        {
          name: 'GROUP TICKETS',
          icon: 'fa-users',
          isActive: false
        },
        {
          name: 'INVESTORS',
          icon: 'fa-crosshairs',
          isActive: false
        },
        {
          name: 'STARTUPS',
          icon: 'fa-lightbulb-o',
          isActive: false
        }
      ]
    }
  },
  methods: {
    toggleActive (index) {
      this.selections.map(selection => {
        selection.isActive = false
      })
      this.selections[index].isActive = true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>
