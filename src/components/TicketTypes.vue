<template>
    <!-- static layout for the ticket types. -->
    <div class="container my-5">
      <div class="row">
        <!-- ticket types for mobile view (stacked to one another) -->
        <div class="col-12 d-block d-md-none text-center">
          <ul class="list-unstyled">
            <li class="py-1">
              <span class="text-uppercase text-blue">early bird</span>&nbsp;
              <span class="span-blue text-uppercase small-font-sm font-weight-bold">sold out</span>
            </li>
            <li class="py-1">
              <span class="text-uppercase text-blue">summer saver</span>
            </li>
            <li class="py-1">
              <span class="text-uppercase text-active font-weight-bold">Regular</span>
              <span class="text-uppercase">&nbsp;
                <i class="fa fa-clock-o fa-lg"></i>
                <span class="small-font-sm">until</span>&nbsp;
                <span class="text-red text-uppercase font-weight-bold small"> aug. 31</span>
              </span>
            </li>
            <li class="py-1">
              <span class="text-uppercase text-blue">late</span>
            </li>
            <li class="py-1">
              <span class="text-uppercase text-blue">onsite registration</span>
            </li>
          </ul>
        </div>
        <!-- mobile view end -->
        <!-- ticket types for large devices (one line) -->
        <div class="col-12 d-none d-md-block text-center">
          <ul class="list-inline">
            <li class="list-inline-item mr-0">
              <span class="text-uppercase text-blue">early bird</span>&nbsp;
              <span class="span-blue text-uppercase small-font font-weight-bold">sold out</span>
              <span class="slash">/</span>
            </li>
            <li class="list-inline-item mr-0">
              <span class="text-uppercase text-blue">summer saver</span>
              <span class="slash-active">/</span>
            </li>
            <li class="list-inline-item mr-0">
              <span class="text-uppercase text-active font-weight-bold">Regular</span>
              <span class="text-uppercase">&nbsp;
                <i class="fa fa-clock-o icon-font"></i>
                <div class="d-inline-block stacked">
                <span class="small-font d-block">until</span>&nbsp;
                <span class="text-red text-uppercase font-weight-bold small d-block"> aug. 31</span>
                </div>
              </span>
              <span class="slash-active">/</span>
            </li>
            <li class="list-inline-item mr-0">
              <span class="text-uppercase text-blue">late</span>
              <span class="slash">/</span>
            </li>
            <li class="list-inline-item mr-0">
              <span class="text-uppercase text-blue">onsite registration</span>
            </li>
          </ul>
        </div>
        <!-- large devices view end -->
      </div>
    </div>
</template>

<script>
export default {
  name: 'ticket-types'
}
</script>

