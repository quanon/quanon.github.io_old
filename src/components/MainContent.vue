<template lang="pug">
  main.column.is-9
    .tabs
      ul
        li.is-active
          a 好きなもの
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
  @import '~bulma/sass/utilities/initial-variables';
  @import '~bulma/sass/utilities/mixins';

  main {
    overflow-y: auto;
  }

  .tabs {
    position: sticky;
    top: 0;
    background-color: white;
  }

  .tiles {
    /*
     * Remove negative mergin ($size-7: 0.75rem) from .tile.is-ancestor
     * to prevent duplicated scroll
     */
    padding: $size-6;
  }

  @media screen and (max-width: $tablet - 1px) {
    .tile .content .column {
      &:not(:first-child) {
        padding-top: 0;

        ul {
          margin-top: 0;
        }

        li:first-child {
          margin-top: 0.25rem;
        }
      }

      &:not(:last-child) {
        padding-bottom: 0;
      }
    }
  }
</style>
