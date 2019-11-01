<template>
    <div>
        <nav class="top">
            <div class="logo">
                <a href="#" id="logo">
                    <img src="../assets/Images/logo-horizontal-1.png" />
                </a>
            </div>
            <ul class="navBar">
                <li><a href="#" id="soFunk" >SO FUNKTIONIERT’S</a></li>
                <li><a href="#" id="sonder" >SONDERANGEBOTE</a></li>
                <li><dropdown :on-click="changeMenuItem" :items="menuItems" class="dropdown"></dropdown></li>
            </ul>
        </nav>
    </div>
</template>

<script>
import Dropdown from './Dropdown'
export default {
    name: "MenuBar",

    components: {
        Dropdown,
    }
}
</script>

<style lang="scss">
  nav {
    background-color: #303030;
    display: inline-flex;
    width: 100%;
    justify-content: space-evenly;
    align-items: center;
  }
    .navBar {
        margin-block-start: 0;
        margin-block-end: 0;
    }
  ul li {
      display: inline;
  };
  ul li a {
    color: white;
    display: inline;
    align-items: center;
    vertical-align: middle;
    padding:0px 19px;
    text-decoration: none;
    font-weight: 600;
    font-family: Montserrat;
    font-size: 15px;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: normal;
  }
  .logo {
      display: inline-block;
      vertical-align: middle;
      padding: 0.5em;
  }
  .dropdown {
    display: inline-block;
  }

  
</style>