<template>
  <div>
    <Menu />
    <div class="container mt-5">
      <nuxt />
    </div>
  </div>
</template>


<script>
import Menu from '~/components/Menu';
export default {
    name: "defaultlayout",
    components:{
      Menu
    }
}
</script>
<style>
body{
  font-weight: 600;
  font-size: 18px;
  background: rgb(247, 246, 246);
}
</style>
