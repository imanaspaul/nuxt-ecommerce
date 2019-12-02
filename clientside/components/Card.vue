<template>
<div class="row my-5">
  <div v-for="product in products" :key="product.id" class="col-sm-6 col-lg-3 col-md-4  mb-4">
      <div class="product" style="width:100%">
          <div class="card" style="width:100%">
          <img :src="product.image" class="card-img-top" alt="appple" style="height:230px;">
          <div class="card-body">
              <p>{{ product.name }}</p>
              <p class="text-muted">MPR: {{ product.Price }}/Kg</p>
          </div>
      </div>
      <div v-if="product.Instock" class="ribbonInStock">
          In Stock
      </div>
      <!-- <div v-if="!product.Instock" class="ribbonOutOfStock">
          Out of Stock
      </div> -->
      <div v-if="!product.Instock" class="overlay text-center">
          <h5 class="mt-5 pt-5">Out Of Stock</h5>
          <h5 class="mb-5 pb-5">Will Be Restored Soon</h5>
      </div>
      </div>
  </div>
  </div>
</template>

<script>
export default {
    name: "card",
    data(){
        return{
            Instock: false,
            products: [
                {
                    id: 1,
                    name: "Apple",
                    image: "https://images.pexels.com/photos/102104/pexels-photo-102104.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500",
                    Instock: true,
                    Price: 230
                },
                {
                    id: 2,
                    name: "Mango",
                    image: "https://plantogram.com/wa-data/public/shop/products/55/06/655/images/1256/1256.970.jpg",
                    Instock: false,
                    Price: 230
                },
                 {
                    id: 3,
                    name: "Banana",
                    image: "https://upload.wikimedia.org/wikipedia/commons/8/8a/Banana-Single.jpg",
                    Instock: true,
                    Price: 230
                },
                {
                    id: 4,
                    name: "Mango",
                    image: "https://plantogram.com/wa-data/public/shop/products/55/06/655/images/1256/1256.970.jpg",
                    Instock: false,
                    Price: 230
                },
            ]
        }
    }
}
</script>

<style scoped>
.card{
    border: none;
    transition: 1s cubic-bezier(0.075, 0.82, 0.165, 1);
   
}
.card:hover{
    box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15) !important
}
.product{
     position: relative;
}
.ribbonInStock{
    position: absolute;
    top: 0;
    right: 10;
    background-color: rgb(7, 212, 92);
    padding: 3px;
    border-radius: 0px 10px 10px 0px;
    color: white;
}
.ribbonOutOfStock{
    position: absolute;
    top: 0;
    right: 10;
    background-color: rgb(212, 55, 7);
    padding: 3px;
    border-radius: 0px 10px 10px 0px;
    color: white;
}
.overlay{
    position: absolute;
    content: 'Out Of Stock';
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    padding: 10px;
    background-color: rgba(0, 0, 0, 0.363);
    color: white;
}
.overlay span{
    color: red;
    margin-top: 20px;
}
</style>