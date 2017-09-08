<template lang="pug">
  .column.is-9
    .tabs
      ul
        li.is-active
          a 好きなもの
    main
      .tiles
        .tile.is-ancestor(v-for='favorites in favoriteLists')
          .tile.is-parent(v-for='favorite in favorites' v-bind:class='favorite.tileClass')
            .tile.is-child.box
              p.title {{ favorite.title }}
              .content
                .columns(v-if="favorite.itemsList")
                  .column.is-6(v-for='items in favorite.itemsList')
                    ul
                      li(v-for='item in items') {{ item }}
                ul(v-else)
                  li(v-for='item in favorite.items') {{ item }}
</template>

<script>
  import favoriteLists from '@/data/favorites.yml';

  export default {
    data() {
      return {
        favoriteLists
      };
    }
  };
</script>

<style lang="scss" scoped>
  .column {
    overflow-y: auto;
  }

  .tiles {
    margin: 1.0rem;
  }
</style>
