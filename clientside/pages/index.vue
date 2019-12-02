<template>
<div>
  <div class="row">
    <div class="col-md-9">
      <Search/>
    </div>
    <div class="col-md-3">
      <Filterbutton/>
    </div>
  </div>
      <card/>
  </div>
</template>

<script>

import Search from '~/components/Search.vue';
import Filterbutton from '~/components/Filterbutton.vue';
import Card from '~/components/Card.vue';
export default {
  components: {
    Search,
    Filterbutton,
    Card
  }
}
</script>

<style scoped>


</style>
