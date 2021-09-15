<template>
    <header class="header">
        <div class="container">
            <div class="header__inner">
                <div class="header__cleaning">
                    <img
                        class="header__logo"
                        src="../assets/images/logo.svg"
                        alt="logo"
                    />
                    <div class="header__swith">
                        <button
                            class="
                                header__swith-button
                                header__swith-home
                                header__swith-button-active
                            "
                        >
                            Дом
                        </button>
                        <button
                            class="header__swith-button header__swith-office"
                        >
                            Офис
                        </button>
                    </div>
                </div>
                <nav class="header__nav">
                    <ul class="header__nav-list">
                        <li class="header__nav-list-item">
                            <a href="#" class="header__nav-list-link">
                                После ремонта</a
                            >
                        </li>
                        <li class="header__nav-list-item">
                            <a href="#" class="header__nav-list-link"
                                >Генеральная уборка</a
                            >
                        </li>
                        <li class="header__nav-list-item">
                            <a href="#" class="header__nav-list-link"
                                >Регулярная уборка</a
                            >
                        </li>
                        <li class="header__nav-list-item">
                            <a href="#" class="header__nav-list-link">
                                Мойка окон
                            </a>
                        </li>
                    </ul>
                </nav>
                <div class="header__contacts">
                    <div class="header__contacts-inner">
                        <a
                            class="header__contacts-link"
                            href="tel:+380 67 401 69 77"
                        >
                            +380 67 401 69 77</a
                        >
                        <span>|</span>
                        <span class="header__contacts-support">27/7</span>
                    </div>

                    <div class="header__contacts-menu">
                        <span class="header__contacts-menu-line"></span>
                        <span class="header__contacts-menu-line"></span>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'AppHeader',
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/_mixin.scss';

.header {
}

.header__inner {
    @include myFlex;
}
.header__cleaning {
    @include myFlex;
    width: 250px;
    max-width: 250px;
}
.header__logo {
    width: 100px;
    height: 25px;
}
.header__swith {
    width: 131px;
    height: 30px;
    border-radius: 48px;
    border: 3px solid $primary-color;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.header__swith-button {
    width: 55px;
    height: 31px;
    border-radius: 34px;
    color: $text-secondary;
    border: none;
    cursor: pointer;
    font-family: 'TTTravels-Regular', sans-serif;
    font-size: 14px;
    background-color: $primary-color;
}
.header__swith-button:active,
.header__swith-button:focus {
    outline: none;
}
.header__swith-home {
}
.header__swith-office {
}
.header__swith-button-active {
    background-color: $purple-color;
    color: $primary-color;
}
.header__nav {
}
.header__nav-list {
    @include myFlex;
    color: $black-color;
    font-size: 16px;
    font-family: 'TTTravels-Regular', sans-serif;
    width: 662px;
    max-width: 662px;
    cursor: pointer;
}
.header__nav-list-item {
    list-style-type: none;
}
.header__nav-list-link {
    text-decoration: none;
    color: $black-color;
}
.header__contacts {
    @include myFlex;
    width: 292px;
    max-width: 292px;
    font-family: 'TTTravels-Medium', sans-serif;
    font-size: 16px;
}
.header__contacts-inner {
    @include myFlex;
    letter-spacing: 0.2px;
    width: 228px;
    max-width: 228px;
}

.header__contacts-link {
    color: $black-color;
    text-decoration: none;
}
.header__contacts-support {
}

.header__contacts-menu {
    width: 32px;
    height: 32px;
    position: relative;
    cursor: pointer;
}
.header__contacts-menu-line {
    &:first-child {
        position: absolute;
        top: 11px;
        left: 5px;
        width: 20px;
        height: 2px;
        background-color: $black-color;
    }
    &:last-child {
        position: absolute;
        bottom: 11px;
        left: 5px;
        width: 20px;
        height: 2px;
        background-color: $black-color;
    }
}
</style>
