<script setup></script>

<template>
  <header class="header">
    <div class="header__extentions container">
      <div class="header__extentions-inner">
        <a class="header__extentions-logo">
          <img src="../assets/images/logo-white.svg" alt="Logo" loading="lazy" />
        </a>

        <!-- Взять стили как основу для кнопки -->
        <button style="position: relative; width: 100px; height: 200px">
          <img
            src="../assets/images/icon-sun.svg"
            alt=""
            style="
              background-color: black;
              position: absolute;
              width: 100px;
              height: 100%;
              object-fit: fill;
              top: 0;
              left: 0;
            "
          />
        </button>
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss"></style>
