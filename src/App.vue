<template>
  <div id="app">
    <selection></selection>
    <ticket-types></ticket-types>
    <cards></cards>
  </div>
</template>

<script>
import Selection from './components/Selection'
import TicketTypes from './components/TicketTypes'
import Cards from './components/Cards'

export default {
  name: 'app',
  components: {
    Selection,
    TicketTypes,
    Cards
  }
}
</script>