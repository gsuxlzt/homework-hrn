<template>
    <div class="container my-5">
      <div class="row">
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
                <i class="fa fa-clock-o"></i>
                <span class="small-font-sm">until</span>&nbsp;
                <span class="text-danger text-uppercase font-weight-bold small">sept. 30</span>
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
                <i class="fa fa-clock-o"></i>
                <span class="small-font">until</span>&nbsp;
                <span class="text-danger text-uppercase font-weight-bold small">sept. 30</span>
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
      </div>
    </div>
</template>

<script>
export default {
  name: 'ticket-types'
}
</script>

