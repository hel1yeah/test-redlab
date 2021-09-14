<template>
  <header class="header">
    <div class="container">
      <div class="header__inner">
        <div class="header__cleaning">
          <img class="header__logo" src="" alt="" />
          <div class="header__swith">
            <button class="header__swith-button header__swith-home">Дом</button>
            <button class="header__swith-button header__swith-office">
              Офис
            </button>
          </div>
        </div>
        <nav class="header__nav">
          <ul class="header__nav-list">
            <li class="header__nav-list-item">После ремонта</li>
            <li class="header__nav-list-item">Генеральная уборка</li>
            <li class="header__nav-list-item">Регулярная уборка</li>
            <li class="header__nav-list-item">Мойка окон</li>
          </ul>
        </nav>
        <div class="header__contacts">
          <a class="header__contacts-link" href="tel:+380 67 401 69 77">
            +380 67 401 69 77</a
          >
          <span class="header__contacts-support">27/7</span>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
};
</script>

<style lang="scss" scoped></style>
