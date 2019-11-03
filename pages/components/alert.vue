<template>
  <div class="container-fluid">
    <h1>Alertes</h1>
    <h2>Sans icônes</h2>
    <div class="row">
      <Alert/>
      <Alert type="info"/>
      <Alert type="warning"/>
      <Alert type="danger"/>
    </div>
    <h2>Avec icônes</h2>
    <div class="row">
      <Alert icon="check"/>
      <Alert type="info" icon="info"/>
      <Alert type="warning" icon="warning"/>
      <Alert type="danger" icon="error"/>
    </div>
    <h2>Avec bordure</h2>
    <Alert icon="check" :bordered="true"/>
    <Alert type="info" icon="info" :bordered="true"/>
    <Alert type="warning" icon="warning" :bordered="true"/>
    <Alert type="danger" icon="error" :bordered="true"/>
    <h2>Avec fermeture</h2>
    <Alert icon="check" :close="true" :onClose="onClose"/>
    <Alert type="info" icon="info" :bordered="true" :close="true" :onClose="onClose"/>
  </div>
</template>

<script>
  import Alert from "../../components/Alert";

  export default {
    name: "alert",
    components: {Alert},
    methods: {
      onClose() {
        alert('Alerte se ferme.');
      }
    },
    transition: 'slide-down',
  }
</script>
