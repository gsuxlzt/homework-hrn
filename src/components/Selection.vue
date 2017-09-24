<template>
  <div class="container-fluid bg-gray has-shadow height-maxed">
    <div class="container">
      <!-- the selections below the navbar. will be rendered dynamically -->
      <div class="row no-gutters align-items-center justify-content-center sm-stacked py-2 py-sm-3 py-md-2 py-lg-3">
        <div class="col-3 text-center fixed-height" v-for="(selection,index) in selections" :key="index">
         <!-- clicking the corresponding icon will make it active
         (change color, arrow pointing down) -->
          <a class="small-font-sm selection no-underline" 
            :class="{'is-active' : selection.isActive}" 
            href="#" 
            @click="toggleActive(index)">
            <i :class="selection.icon" class="fa icon-font fa-fw d-block mx-auto d-sm-inline-block"></i>
            <span> {{ selection.name }}</span>
          </a>
        </div>
      </div>
      <!-- selections end -->
    </div>
  </div>
</template>

<script>
export default {
  name: 'selection',
  data () {
    return {
      // each selection
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
    // for adding the active class to the selection
    toggleActive (index) {
      this.selections.map(selection => {
        selection.isActive = this.selections[index] === selection
      })
    }
  }
}
</script>