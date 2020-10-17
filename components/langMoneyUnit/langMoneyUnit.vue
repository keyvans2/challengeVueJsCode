<template>
  <div>
    <div class="langMoney">
      <div class="langs">
        <p>زبان</p>
        <div>فارسی</div>
        <div>English</div>
      </div>
      <div class="units">
        <p>واحد پول</p>
        <div>دلار</div>
        <div>تومان</div>
        <div>لیر</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
.langMoney {
  width: 200px;
  height: auto;
  background-color: rgb(32, 34, 40);
  position: absolute;
  z-index: 999;
  left: 0;
  .langs {
    width: 50%;
    height: 100%;
    // background-color: cyan;
    float: right;
    p {
      text-align: right;
      margin: center;
      padding-right: 20px;
      font-size: 12px;
      height: 40px;
      line-height: 40px;
      color: rgb(174, 180, 188);
    }
    div {
      width: 100%;
      height: 40px;
      line-height: 40px;
      padding-right: 20px;
      &:hover {
        background-color: rgb(38, 38, 42);
         color: #f0b90b;
      }
    }
  }
  .units {
    width: 50%;
    height: 100%;
    float: left;
     p {
      text-align: right;
      margin: center;
      padding-right: 20px;
      font-size: 12px;
      height: 40px;
      line-height: 40px;
      color: rgb(174, 180, 188);
    }
    div {
      width: 100%;
      height: 40px;
      line-height: 40px;
      padding-right: 20px;
      &:hover {
        background-color: rgb(38, 38, 42);
         color: #f0b90b;
      }
    }
  }
}
</style>