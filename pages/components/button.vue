<template>
  <div class="container-fluid">
    <h1>Bouttons</h1>
    <h2>Flat</h2>
    <Button type="flat" content="Normal"/>
    <Button type="flat" content="Blue" color="blue"/>
    <Button type="flat" content="Red" color="red"/>
    <Button type="flat" content="Orange" color="orange"/>
    <Button type="flat" content="Green" color="green"/>
    <h2>Color</h2>
    <Button content="Normal"/>
    <Button content="Blue" color="blue"/>
    <Button content="Red" color="red"/>
    <Button content="Orange" color="orange"/>
    <Button content="Green" color="green"/>
    <h2>Outlined</h2>
    <Button content="Normal" type="outlined"/>
    <Button content="Blue" color="blue" type="outlined"/>
    <Button content="Red" color="red" type="outlined"/>
    <Button content="Orange" color="orange" type="outlined"/>
    <Button content="Green" color="green" type="outlined"/>
    <h2>With icons</h2>
    <Button content="Normal" icon="info"/>
    <Button content="Blue" color="blue" icon="info"/>
    <Button content="Red" color="red" icon="error"/>
    <Button content="Orange" color="orange" icon="warning"/>
    <Button content="Green" color="green" icon="check"/>
    <h2>Size</h2>
    <Button content="Small" color="blue" size="small"/>
    <Button content="Default" color="blue" size="default"/>
    <Button content="Large" color="blue" size="large"/>
    <h2>Elevation</h2>
    <Button content="Elevation XL" color="blue" size="default" class="elevation-xl"/>
    <Button content="Elevation LG" color="blue" size="default" class="elevation-lg"/>
    <Button content="Elevation MD" color="blue" size="default" class="elevation-md"/>
    <h2>Rounded</h2>
    <Button content="Rounded button" color="green" size="default" class="elevation-xl" rounded/>
  </div>
</template>

<script>
  import Button from "../../components/Button";

  export default {
    name: "button",
    transition: 'slide-down',
    components: {Button},
  }
</script>

<style scoped>

</style>
