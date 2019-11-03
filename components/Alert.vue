<template>
  <div role="alert" class="alert" :class="[`alert__${type}`, this.borderedClass]">
    <div class="alert__wrapper">
      <i class="material-icons alert__wrapper--icon" v-if="icon">{{ icon }}</i>
      <div class="alert__wrapper--content">{{ content }}</div>
      <div class="alert__wrapper--close" v-if="close" @click="onClose()">
        <i class="material-icons">close</i>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Alert",
    props: {
      content: {
        type: String,
        default: 'Ceci est une alerte',
      },
      type: {
        type: String,
        default: 'success',
        validator: function(value) {
          return ['success', 'warning', 'danger', 'info'].indexOf(value) !== -1
        }
      },
      icon: {
        type: String,
      },
      bordered: {
        type: Boolean,
        default: false,
      },
      close: {
        type: Boolean,
        default: false,
      },
      onClose: {
        type: Function,
        default: () => {},
      }
    },
    computed: {
      borderedClass: function() {
        if (!this.bordered) {
          return;
        }

        return `alert__bordered alert__bordered--${this.type}`;
      }
    }
  }
</script>
