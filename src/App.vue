<template>
  <div id="app">
    <selection></selection>
    <ticket-types></ticket-types>
    <cards></cards>
    <partners></partners>
  </div>
</template>

<script>
import Selection from './components/Selection'
import TicketTypes from './components/TicketTypes'
import Cards from './components/Cards'
import Partners from './components/Partners'

export default {
  name: 'app',
  components: {
    Selection,
    TicketTypes,
    Cards,
    Partners
  }
}
</script>