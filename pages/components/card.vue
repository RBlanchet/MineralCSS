<template>
  <div class="container-fluid">
    <h1>Cards</h1>
    <div class="row">
      <div class="col-md-6">
        <Card class="elevation-xl"/>
      </div>
    </div>
    <h2>Card avec image</h2>
    <div class="row mb-5">
      <div class="col-md-6">
        <Card class="elevation-xl" img="https://images.unsplash.com/photo-1513618827672-0d7c5ad591b1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80"/>
      </div>
      <div class="col-md-6">
        <Card class="elevation-xl" img="https://images.unsplash.com/photo-1446292267125-fecb4ecbf1a5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80" alt="Une autre image" color="white"/>
      </div>
    </div>
    <h2>Card de couleur</h2>
    <div class="row mb-5">
      <div class="col-md-6">
        <Card class="elevation-xl" color="blue"/>
      </div>
      <div class="col-md-6">
        <Card class="elevation-xl" color="red"/>
      </div>
    </div>
    <h2>Avec pied de page</h2>
    <div class="row mb-5">
      <div class="col-md-6">
        <Card class="elevation-xl" color="blue">
          <template v-slot:footer>
            <div class="row w-100 flex justify-content-end">
              <Button/>
            </div>
          </template>
        </Card>
      </div>
      <div class="col-md-6">
        <Card class="elevation-xl">
          <template v-slot:footer>
            <div class="row w-100 flex justify-content-end">
              <Button type="flat" color="blue" content="J'aime !" icon="thumb_up" rounded/>
              <Button type="flat" color="red" content="J'aime pas !" icon="thumb_down" rounded/>
            </div>
          </template>
        </Card>
      </div>
    </div>
  </div>
</template>

<script>
  import Card from "../../components/Card";
  import Button from "../../components/Button";

  export default {
    name: "card",
    components: {Card, Button},
    transition: 'slide-down',
  }
</script>
