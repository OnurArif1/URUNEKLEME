<template>
  <div class="container">
    <h1 class="text-center">Ürün Ekleme Uygulaması</h1>
    <hr>
    <app-new-product></app-new-product>
    <br><br>
    <app-progress></app-progress>
    <br><br>
    <h3 class="text-center">Eklenen Ürünlerin Listesi</h3>
    <hr>
    <app-product></app-product>
  </div>
</template>

<script>
  import AppNewProduct from "./component/NewProduct.vue";
  import AppProgress from "./component/Progress.vue";
  import AppProduct from "./component/Product.vue";

  export default 
  {
    components:
    {
      AppNewProduct,
      AppProgress,
      AppProduct 
    },
    methods: 
    {
      onChange(e) 
      {
        const file = e.target.files[0];
        this.product.selectedImage = URL.createObjectURL(file);
      }
    }
  }
</script>

<style>
  body {
    background-color: aliceblue;
    padding-top: 20px;
    padding-bottom: 20px;
  }

  .card{
    margin-right: 5px;
    margin-bottom: 5px;
  }

  .card:last-child{
    margin-right: 0px;
  }

  .col-md-2{
    max-width: 15.666667%!important;
  }

  .product-container{
    margin-left: 15px;
  }

</style>

