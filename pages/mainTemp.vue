<template>
  <div>
      <main-top-menu-navs class="mainTopMenu"/>
    <right-menu-content class="rightContentM"/>
    <div class="leftContent">
      <nuxt-child />
    </div>
  </div>
</template>
<script>
import rightMenuContent from "~/components/desktopContent/rightMenuContent";
import mainTopMenuNavs from "~/components/mobileContent/mainTopMenuNavs";
export default {
  components: {
    rightMenuContent,
    mainTopMenuNavs
  },
};
</script>
<style lang="less" scoped>
.leftContent {
  width:85%;
  height:auto;
//   background-color: red;
  float: left;
}
@media only screen and (max-width: 766px) {
  .rightContent {
    display: none;
  }

  .leftContent{
      width: 100%;
  }
}
@media only screen and (max-width: 1240px) {
 

  .leftContent{
      width: 80%;
  }
}
@media only screen and (max-width: 900px) {
 

  .leftContent{
      width: 76%;
  }
}
@media only screen and (min-width: 766px) {
  .mainTopMenu{
      display: none;
  }
}
@media only screen and (max-width: 766px) {
  .rightContentM{
      display: none;
  }
  .leftContent{
      width: 100%;
  }
}
</style>