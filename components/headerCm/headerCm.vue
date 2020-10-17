<template>
  <div>
    <header>
      <mobile-toggle-menu
        :acrd="acrd"
        @close="acrd = false"
        @closea="acrd = false"
        ref="test"
      />
      <div class="rightPartHeader">
        <div class="logo">
          <img src="../../assets/logo.svg" title="mrBitTex" alt="logo" />
        </div>
        <div class="markets">
          <a href="http://">بازارها</a>
        </div>
      </div>
      <div class="leftPartHeader">
        <left-part-nav-desktop class="navDesktop" />
        <left-part-nav-mobile @acardeon="acrd = true" />
      </div>
    </header>
    <div class="toggleMenuBack" @click="closeAcr" v-if="acrd"></div>
  </div>
</template>

<script>
import leftPartNavDesktop from "~/components/leftPartDesktopHeader/leftPartDesktopHeader";
import leftPartNavMobile from "~/components/mobileLeftNav/mobileLeftNav";
import mobileToggleMenu from "~/components/mobileToggleMenu/mobileToggleMenu";
export default {
  created() {
    if (process.client) {
      let t = this;

      // window.addEventListener("click", this.checkEl);
    }
  },
  data() {
    return {
      acrd: false,
    };
  },
  methods: {
    closeAcr() {
      this.acrd = false;
    },
  },
  components: {
    leftPartNavDesktop,
    leftPartNavMobile,
    mobileToggleMenu,
  },
};
</script>

<style lang="less" scoped>
.toggleMenuBack {
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  z-index: 1;
  // background-color: cyan;
}
header {
  height: 64px;
  background-color: rgb(18, 22, 28);
  .rightPartHeader {
    width: 30%;
    height: 100%;
    // background-color: cyan;
    float: right;
    .logo {
      width: 120px;
      height: 100%;
      // background-color: red;
      float: right;

      img {
        width: 100px;
        vertical-align: middle;
        margin: 20px auto;
      }
    }
    .markets {
      padding-right: 20px;
      float: right;
      a {
        display: block;
        text-decoration: none;
        font-weight: 400;
        text-align: center;
        color: #ffffff;
        font-size: 14px;
        margin-top: 20px;
        padding-right: 10px;
        margin-left: 40px;
        font-family: yekan, sans-serif;
      }
      &:hover a {
        color: #f0b90b;
      }
    }
  }
  .leftPartHeader {
    width: 70%;
    height: 100%;
    // background-color: darkblue;
  }
}

@font-face {
  font-family: yekan;
  src: url("../../assets/fonts/YekanBakhRegular.ttf");
}
@media only screen and (max-width: 766px) {
  .markets {
    display: none;
  }
  .navDesktop {
    display: none;
  }
}
</style>