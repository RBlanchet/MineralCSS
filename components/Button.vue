<template>
  <button class="btn"
    :class="[
      `btn__${type}`,
      `btn__${size}`,
      `${color}__text`,
      `${color}`,
      {'rounded__full': rounded},
      {'btn__outlined': type === 'outlined'}
    ]">
    <i class="material-icons btn__icon" v-if="icon">{{ icon }}</i>
    <span class="btn__content">{{ content }}</span>
  </button>
</template>

<script>
  export default {
    name: "Button",
    props: {
      type: {
        type: String,
        default: 'normal',
      },
      size: {
        type: String,
        default: 'default',
      },
      content: {
        type: String,
        default: 'Button',
      },
      color: {
        type: String,
        default: 'white',
        validator: function(value) {
          return ['blue', 'red', 'orange', 'green', 'grey', 'white'].indexOf(value) !== -1
        }
      },
      rounded: {
        type: Boolean,
        default: false,
      },
      icon: {
        type: String,
      },
    }
  }
</script>
