<template lang="pug">
  aside.column.is-3
    figure.image.is-128x128
      img(:src='src')
    .title.is-size-1.has-text-centered QUANON
    .positions.has-text-centered
      p スピリチュアルプログラマ
      p ハルキスト
      p 杏さや教徒
    .websites.has-text-centered
      p
        i.fa.fa-fw.fa-link
      p
        a(href='https://twitter.com/quanon_jp' target='_blank') Twitter (@quanon_jp)
      p
        a(href='https://www.amazon.co.jp/registry/wishlist/2A9GAIXR0O4K' target='_blank') Amazon ウィッシュリスト
      p
        a(href='https://qiita.com/QUANON' target='_blank') Qiita
      p
        a(href='https://github.com/quanon' target='_blank') Github
      p
        a(href='http://quanon.hateblo.jp' target='_blank') はてなブログ
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

    @media screen and (min-width: $tablet) and (max-width: $desktop - 1px) {
      .title {
        font-size: $size-2 !important;
      }
    }

    .image {
      margin-top: $size-4;

      img {
        border-radius: 50%;
      }
    }

    .positions {
      margin-bottom: $size-5;
      font-size: $size-6;
    }

    @media screen and (min-width: $tablet) and (max-width: $desktop - 1px) {
      .positions {
        font-size: $size-7;
      }
    }

    .websites {
      margin-bottom: $size-4;
      font-size: $size-7;

      a {
        color: white;
      }
    }
  }
</style>
