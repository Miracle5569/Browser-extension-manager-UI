<script setup></script>

<template>
  <header class="header">
    <div class="header__extentions container">
      <div class="header__extentions-inner">
        <a class="header__extentions-logo">
          <img src="../assets/images/logo-white.svg" alt="Logo" loading="lazy" />
        </a>

        <button class="header__extentions-change-theme">
          <img
            src="../assets/images/icon-sun.svg"
            alt="Light theme"
            loading="lazy"
            class="header__extentions-icon-theme"
          />
        </button>
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
@use '../assets/style/core' as core;

.header__extentions {
  padding-top: #{core.rem(40)};

  &-inner {
    @include core.flex-jst-center;
    padding: #{core.rem(10)} #{core.rem(20)};
    border-radius: #{core.rem(20)};
    background-color: var(--Neutral-800);
  }

  &-change-theme {
    width: #{core.rem(50)};
    height: #{core.rem(50)};
    outline: none;
    border: none;
    background-color: var(--Neutral-700);
    border-radius: #{core.rem(10)};
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>
