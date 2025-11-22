//NOTE - Внутренняя обработка процесса фильтрайии. На входе пропсом принимать значение эвента и
фильтровать данные исхожя из проспа

<script setup>
const props = defineProps(['e'])
const EVENTS = ['viewAll', 'viewActive', 'viewInactive']

//FIXME - Тестовый сценарий - вынести!!!
const initEvent = (e) => {
  console.log(props.e == EVENTS.find((item) => item == e))
}
</script>

<template>
  <button class="filter" @click="initEvent(props.e)">
    <slot></slot>
  </button>
</template>

<style scoped lang="scss">
@use '../../assets/style/core' as core;

.filter {
  padding: #{core.rem(10)} #{core.rem(20)};
  border-radius: #{core.rem(22)};
  border: none;
  background-color: var(--Neutral-700);
  color: var(--Neutral-0);

  &:hover {
    background-color: var(--Neutral-600);
  }
}
</style>
