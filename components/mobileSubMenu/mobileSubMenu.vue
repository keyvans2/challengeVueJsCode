<template>
  <div>
    <div class="subMenu " >
      <ul>
        <li v-for="(sub, i) in subs" :key="i">
          {{ sub }}
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    subs: {
      type: [Array, Object],
    },
    current: {
      type: Number,
    },
    // acardeon: {
    //   type: false,
    // },
  },
};
</script>

<style lang="less">
.subMenu {
  width: 100%;
  max-height: 0;
  transition: max-height 0.4s ease-in;
  overflow: hidden;
  ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: inline-block;
    width: 100%;
    li {
      width: 100%;
      height: 54px;
      font-size: 16px;
      color: #ffffff;
      padding: 15px 42px 15px 0;
      text-align: right;
      vertical-align: middle;
      font-family: yekan, sans-serif;
      position: relative;

      &:hover {
        // background-color: rgb(32, 34, 40);
        // > i {
        //   // transform: rotate(180deg);
        // }
      }
    }
  }
}

</style>