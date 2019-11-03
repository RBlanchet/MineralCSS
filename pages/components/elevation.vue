<template>
  <div class="container-fluid wrapper">
    <h1>Elevations</h1>
    <div class="row">
      <div class="col-md-12 p-5 mt-5 elevation">elevation</div>
      <div class="col-md-12 p-5 mt-5 elevation-md">elevation-md</div>
      <div class="col-md-12 p-5 mt-5 elevation-lg">elevation-lg</div>
      <div class="col-md-12 p-5 mt-5 elevation-xl">elevation-xl</div>
      <div class="col-md-12 p-5 mt-5 elevation-2xl">elevation-2xl</div>
      <div class="col-md-12 p-5 mt-5 elevation-outline">elevation-outline</div>
      <div class="col-md-12 p-5 mt-5 elevation-inner">elevation-inner</div>
      <div class="col-md-12 p-5 mt-5 elevation-none">elevation-none</div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "elevation",
    transition: 'slide-left',
  }
</script>
