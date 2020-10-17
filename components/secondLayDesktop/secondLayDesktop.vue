<template>
  <div>
    <div class="secondLay">
      <a href="#" v-for="(s, i) in sub" :key="i" :class="{ bullet: bullet }">{{
        s
      }}</a>

      <!-- <a href="#">پیام جدید</a> -->
    </div>
  </div>
</template>
<script>
export default {
  props: {
    sub: {
      type: [Array, Object],
    },
    bullet: {
      type: Boolean,
    },
  },
};
</script>
<style lang="less" scoped>
.secondLay {
  min-width: 150px;
  right: -10px;
  height: auto;
  position: absolute;
  background-color: rgb(32, 34, 40);
  padding: 0;
  margin: 0;
  a {
    display: block;
    width: 100%;
    height: 55px;
    line-height: 55px;
    color: #ffffff;
    text-decoration: none;
    font-family: yekan, sans-serif;
    // font-size: 14px;
    margin: 0;
    padding: 0 12px;
    // margin: 0;
    &:hover {
      background-color: rgb(38, 38, 42);
      color: #f0b90b;
    }
  }
}

.bullet::before {
  content: "";
  box-sizing: border-box;
  min-width: 0px;
  display: inline-block;
  background-color: rgb(240, 185, 11);
  width: 6px;
  height: 6px;
  position: relative;
  transform: rotate(45deg);
  margin-left: 15px;
  margin-right: 5px;
}
</style>

