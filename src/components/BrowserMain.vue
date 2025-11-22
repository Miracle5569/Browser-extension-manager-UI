<script setup>
import NavigationFilter from './navigations/NavigationFilter.vue'

//FIXME - Что-то может быть с этим придумать можно?
const filterList = [
  {
    index: 1,
    name: 'All',
    e: 'viewAll',
    active: true,
  },
  {
    index: 2,
    name: 'Active',
    e: 'viewActive',
    active: false,
  },
  {
    index: 3,
    name: 'Inactive',
    e: 'viewInactive',
    active: false,
  },
]
</script>

<template>
  <main>
    <section class="extentions">
      <header class="extentions__header">
        <div class="extentions__header-inner container">
          <h2 class="extentions__header-title">Extentions List</h2>
          <nav class="extentions__header-navigation">
            <ul class="extentions__header-navigation-list">
              <li
                class="extentions__header-navigation-item"
                v-for="item in filterList"
                :key="item.index"
              >
                <NavigationFilter :e="item.e">{{ item.name }}</NavigationFilter>
              </li>
            </ul>
          </nav>
        </div>
      </header>
      <div class="extentions__body">
        <!-- Список расширений -->
      </div>
    </section>
  </main>
</template>

<style scoped lang="scss">
@use '../assets/style/core' as core;

.extentions {
  &__header {
    margin-top: #{core.rem(50)};

    &-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-block: #{core.rem(20)};
    }

    &-navigation {
      &-list {
        display: flex;

        & > *:not(:last-child) {
          margin-right: #{core.rem(15)};
        }
      }
    }
  }
}
</style>
