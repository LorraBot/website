<template>
    <!-- <nav>
        <div class="container">
            <img class="dc-icon" src="../assets/placeholder.png" />
            <a href="/"><img class="logo" src="../assets/Lora-Transparent.png" /></a>
            <h1>Lorra</h1>
            <div :class="['menu', { 'menu-active': toggled }]">
                <a href="#/commands/">Commands</a>
                <a href="https://support.lorra.xyz/">Help & Support</a>
                <a href="#/dashboard/">Dashboard</a>
            </div>
            <button :class="['hmbgr', { 'active': toggled }]" @click="Hmbgr_Click">
                <span></span>
                <span></span>
                <span></span>
            </button>
        </div>
    </nav> -->

    <header :class="classes.header">
        <div :class="classes.header__content">
            <RouterLink to="/" :class="classes.header__content__logo">Lorra</RouterLink>
            <nav
            :class="[classes.header__content__nav, { toggled }]">
                <ul>
                    <li><a href="#/commands/">Commands</a></li>
                    <li><a href="https://support.lorra.xyz/">Help & Suppor</a></li>
                    <li><a href="#/dashboard/">Dashboard</a></li>
                </ul>
                <button>Login</button>
            </nav>
            <button :class="[classes.header__content__toggle, { 'active': toggled }]" @click="toggle">
                <span></span>
                <span></span>
                <span></span>
            </button>
        </div>
    </header>
</template>
<script lang="ts">
import classes from './Header.module.scss';
export default {
    data() {
        return {
            toggled: false,
            classes
        }
    },
    methods: {
        toggle() {
            this.toggled = !this.toggled;
        }
    }
}
</script>

<style scoped lang="scss">
// @import '~/styles/variables';
// nav {
//     top: 0;
//     left: 0;
//     right: 0;
//     z-index: 99;
//     background-color: map-get($navbar, "background");
//     padding: 16px 32px;
//     border-bottom: 3px solid $primary;
//     transition: 0.4s ease;
//     .container {
//         max-width: 1280px;
//         margin: 0 auto;
//         display: flex;
//         align-items: center;
//         justify-content: space-between;
//         .dc-icon {
//             position: relative;
//             width: 50px;
//             margin: -5px 0 -5px -15px;
//             border-radius: 50%;
//             @media screen and (max-width: $mobile) {
//                 position: flex;
//                 float: right;
//             }
//         }
//         .logo {
//             position: relative;
//             width: 50px;
//             float: left;
//             left: 0;
//             margin: 0 auto;
//         }
//         h1 {
//             color: #fff;
//             font-size: 28px;
//             font-weight: 900;
//             letter-spacing: 2px;
//             padding-left: 10px;
//             @media screen and (max-width: $mobile) {
//                 display: none;
//             }
//         }
//         .hmbgr {
//             display: block;
//             position: relative;
//             z-index: 1;
            
//             user-select: none;

//             appearance: none;
//             border: none;
//             outline: none;
//             background: none;
//             cursor: pointer;
//             span {
//                 display: block;
//                 width: 33px;
//                 height: 2px;
//                 margin-bottom: 5px;
//                 position: relative;

//                 background-color: $light;
//                 border-radius: 6px;
//                 z-index: 1;

//                 transform-origin: 0 0;
//                 transition: 0.4s;
//             }
//             &:hover span:nth-child(2) {
//                 transform: translateX(8px);
//                 background-color: $primary;
//             }
//         }
//         .active {
//             span:nth-child(1) {
//                 transform: translate(0px, -5px) rotate(45deg);
//             }
//             span:nth-child(2) {
//                 opacity: 0;
//                 transform: translateX(15px);
//             }
//             span:nth-child(3) {
//                 transform: translate(-2px, 4px) rotate(-45deg);
//             }
//             &:hover span {
//                 background-color: $primary;
//             }
//             .menu {
//                 display: flex;
//             }
//         }
//         .menu {
//             display: none;
//             flex: 1 1 0%;
//             justify-content: flex-end;
//             margin: 0 -16px;
//             a {
//                 color: #fff;
//                 margin: 0 16px;
//                 font-weight: 400;
//                 font-size: 14px;
//                 text-decoration: none;
//                 transition: 0.4s;
//                 padding: 8px 16px;
//                 border-radius: 20px;
//                 &:hover {
//                     box-shadow: 0 0 2px #fff;
//                 }
//             }
//         }
//         .menu-active {
//             display: none;
//         }
//         @media screen and (min-width: $mobile) {
//             .menu {
//                 display: flex;
//             }
//             .hmbgr {
//                 display: none;
//             }
//         }
//     }
// }
</style>