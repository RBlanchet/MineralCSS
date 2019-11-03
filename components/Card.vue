<template>
  <div class="card" :class="[this.color]">
    <div class="card__background" v-if="img">
      <div class="card__background--img" :style="{'background': `linear-gradient(rgba(0, 0, 0, 0.1), rgba(0, 0, 0, 0.5)), url('${img}')`}"></div>
      <p class="card__background--alt">{{ alt }}</p>
    </div>
    <div class="card__wrapper">
      <h2 class="card__wrapper--title">{{ title }}</h2>
      <article class="card__wrapper--content">{{ content }}</article>
    </div>
  </div>
</template>

<script>
  import { LOREM_SHORT } from './../modules/loremIpsum';
  export default {
    name: "Card",
    props: {
      title: {
        type: String,
        default: 'Titre de ma card',
      },
      content: {
        type: String,
        default: LOREM_SHORT,
      },
      color: {
        type: String,
        default: 'white',
        validator: function(value) {
          return ['blue', 'red', 'orange', 'green', 'grey', 'white'].indexOf(value) !== -1
        }
      },
      img: {
        type: String,
      },
      alt: {
        type: String,
        default: 'Image de la card'
      }
    },
  }
</script>
