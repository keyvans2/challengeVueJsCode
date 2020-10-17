<template>
  <div>
    <div class="toggleMenu" v-if="acrd">
      <div class="items">
        <div class="title" @click="acr(1)">
          <i class="fas fa-sort-up up" v-if="current === 1"></i>
          <i class="fas fa-sort-down down" v-if="current != 1"></i>
          سفارشات
          <svg
            aria-hidden="true"
            focusable="false"
            width="24"
            height="24"
            class="icon note"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
          >
            <path
              d="M9.707 12.729h4.5v-2h-4.5v2zM9.707 16.729h4.5v-2h-4.5v2z"
            ></path>
            <path
              d="M13.5 3.3H5.7v17.5h12.5V7.9l-4.7-4.6zm2.7 15.5H7.7V5.3h5v3.5h3.5v10z"
            ></path>
          </svg>
        </div>
        <div class="subMenus" :class="{ active: current === 1 }">
          <div class="subItems">سفارشات باز</div>
          <div class="subItems">تاریخچه سفارشات</div>
          <div class="subItems">تاریخچه معاملات</div>
        </div>
      </div>
      <div class="items">
        <div class="title" @click="acr(2)">
          <i class="fas fa-sort-up up" v-if="current === 2"></i>
          <i class="fas fa-sort-down down" v-if="current != 2"></i>
          کیف پول
          <svg
            aria-hidden="true"
            focusable="false"
            width="24"
            height="24"
            class="icon wallet"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
          >
            <path
              d="M6.093 8.889c-.567 0-1.031-.438-1.031-.972 0-.535.464-.973 1.03-.973h12.846V5H6.093C4.38 5 3 6.303 3 7.917v8.166C3 17.697 4.381 19 6.093 19H21V8.889H6.093zm12.845 8.167H6.093c-.567 0-1.031-.438-1.031-.973v-5.415c.33.107.68.165 1.03.165h12.846v6.223z"
            ></path>
            <path
              d="M15.845 12.573l-1.453 1.371 1.453 1.38 1.464-1.38-1.464-1.37z"
            ></path>
          </svg>
        </div>
        <div class="subMenus" :class="[{ active: current === 2 }]">
          <div class="subItems">موجودی</div>
          <div class="subItems">واریز</div>
          <div class="subItems">برداشت</div>
        </div>
      </div>
      <div class="items">
        <div class="title" @click="acr(3)">
          <i class="fas fa-sort-up up" v-if="current === 3"></i>
          <i class="fas fa-sort-down down" v-if="current != 3"></i>
          پیام به پشتیبانی
          <svg
            aria-hidden="true"
            focusable="false"
            width="24"
            height="24"
            class="icon chat"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
          >
            <path
              d="M20 15H13.2L9 19.2V15H4V5H20V15ZM22 3H2V17H7V22H9L14 17H22V3Z"
            ></path>
            <path d="M18 7H6V9H18V7Z"></path>
            <path d="M18 11H6V13H18V11Z"></path>
          </svg>
        </div>
        <div class="subMenus" :class="[{ active: current === 3 }]">
          <div class="subItems">لیست پیام ها</div>
          <div class="subItems">پیام جدید</div>
        </div>
      </div>
      <div class="items">
        <div class="title">
          بازارها
          <svg
            aria-hidden="true"
            focusable="false"
            width="24"
            height="24"
            class="icon spot"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 1024 1024"
          >
            <path
              d="M618.666667 192c-89.6 0-166.4 55.466667-196.266667 136.533333 29.866667 0 59.733333 8.533333 85.333333 21.333334 21.333333-42.666667 64-72.533333 110.933334-72.533334 68.266667 0 123.733333 55.466667 123.733333 123.733334 0 51.2-29.866667 93.866667-72.533333 110.933333 12.8 25.6 17.066667 55.466667 21.333333 85.333333 81.066667-29.866667 136.533333-106.666667 136.533333-196.266666 4.266667-115.2-89.6-209.066667-209.066666-209.066667zM401.066667 499.2c68.266667 0 123.733333 55.466667 123.733333 123.733333 0 68.266667-55.466667 123.733333-123.733333 123.733334-68.266667 0-123.733333-55.466667-123.733334-123.733334 0-68.266667 55.466667-123.733333 123.733334-123.733333z m0-85.333333c-115.2 0-209.066667 93.866667-209.066667 209.066666s93.866667 209.066667 209.066667 209.066667 209.066667-93.866667 209.066666-209.066667-93.866667-209.066667-209.066666-209.066666zM870.4 661.333333v213.333334h-213.333333v-85.333334h128v-128h85.333333zM149.333333 149.333333h213.333334v85.333334h-128v128h-85.333334v-213.333334z"
            ></path>
            <path
              d="M870.4 874.666667h-213.333333v-85.333334h128v-128h85.333333v213.333334zM362.666667 149.333333v85.333334h-128v128h-85.333334v-213.333334h213.333334z"
            ></path>
          </svg>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import mobileSubMenu from "~/components/mobileSubMenu/mobileSubMenu";
export default {
  data() {
    return {
      acardeon: false,
      current: 1,
    };
  },
  props: {
    acrd: {
      type: Boolean,
    },
  },
  components: {
    mobileSubMenu,
  },
  methods: {
    acr(val) {
      if (this.current == val) {
        this.current = "";
      } else {
        this.current = val;
      }

      this.acardeon = !this.acardeon;
    },
  },
};
</script>

<style lang="less" scoped>
.toggleMenu {
  position: absolute;
  height: 100vh;
  right: 0px;
  top: 0px;
  bottom: 0px;
  width: 50vw;
  max-width: 240px;
  z-index: 2;
  background-color: rgb(18, 22, 28);
  .items {
    width: 100%;
    height: auto;
    .title {
      text-align: right;
      color: #ffffff;
      font-family: yekan, sans-serif;
      font-size: 16px;
      padding: 15px 10px;
      svg {
        vertical-align: middle;
        margin-right: 9px;
        margin-left: 5px;
        color: rgb(174, 180, 188);
        fill: rgb(174, 180, 188);
      }
      .down {
        float: left;
        margin-left: 10px;
        font-size: 10px;
        margin-top: 5px;
      }
      .up {
        float: left;
        margin-left: 10px;
        font-size: 10px;
        margin-top: 7px;
      }
      &:hover {
        background-color: rgb(32, 34, 40);
      }
    }
    .subMenus {
      width: 100%;
      max-height: 0;
      overflow: hidden;
      //   background-color: dodgerblue;
      transition: max-height 0.4s ease-in;
      .subItems {
        width: 100%;
        height: 54px;
        background-color: rgb(18, 22, 28);

        text-align: right;
        color: #ffffff;
        font-family: yekan, sans-serif;
        padding: 15px 43px;
        &:hover {
          background-color: rgb(32, 34, 40);
        }
      }
    }
  }
}
.active {
  max-height: 200px !important;
  //   overflow: hidden;
  transition: max-height 0.4s ease-in;
}
@media only screen and (min-width: 766px) {
  .toggleMenu {
    display: none;
  }
}
</style>