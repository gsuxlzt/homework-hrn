<template>
  <div id="app">
    <selection></selection>
    <ticket-types></ticket-types>
  </div>
</template>

<script>
import Selection from './components/Selection'
import TicketTypes from './components/TicketTypes'

export default {
  name: 'app',
  components: {
    Selection,
    TicketTypes
  }
}
</script>