<template lang="pug">
  aside.column.is-3
    figure.image.is-128x128
      img(:src='src')
    .title.is-size-1.has-text-centered QUANON
    .positions.has-text-centered
      p スピリチュアルプログラマ
      p ハルキスト
      p 杏さや教徒
    .icons
      a(href='https://twitter.com/quanon_jp' target='_blank')
        i.fa.fa-twitter.is-size-3
      a(href='https://github.com/quanon' target='_blank')
        i.fa.fa-github.is-size-3
      a(href='https://www.amazon.co.jp/registry/wishlist/2A9GAIXR0O4K' target='_blank')
        i.fa.fa-amazon.is-size-3
</template>

<script>
import logo from '@/assets/images/natsuki.png';

export default {
  data() {
    return {
      src: logo
    };
  }
};
</script>

<style lang="scss" scoped>
  @import '~bulma/sass/utilities/initial-variables';

  aside {
    background-color: #563d7c;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: white;

    .title {
      margin: $size-5 0;
      color: white;
    }

    .image {
      margin-top: 1.5rem;

      img {
        border-radius: 50%;
      }
    }

    .positions {
      margin-bottom: $size-5;
      font-size: $size-6;
    }

    .icons {
      margin-bottom: 1.5rem;

      a {
        color: white;
      }

      a:not(first-child) {
        margin-right: 0.5rem;
      }
    }
  }
</style>
