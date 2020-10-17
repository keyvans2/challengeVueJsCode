<template>
  <div>
    <div class="rightContent">
      <div class="items">
        <div class="title" @click="acr(1)">
          <i class="fas fa-sort-up up" v-if="current === 1"></i>
          <i class="fas fa-sort-down down" v-if="current != 1"></i>

          <span> کیف پول </span>

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
              fill="currentColor"
            ></path>
            <path
              d="M15.845 12.573l-1.453 1.371 1.453 1.38 1.464-1.38-1.464-1.37z"
            ></path>
          </svg>
        </div>
        <div class="subMenus" :class="{ active: current === 1 }">
          <div class="subItems">
            <nuxt-link to="#"> موجودی </nuxt-link>
          </div>
          <div class="subItems">
            <nuxt-link
              tag="a"
              :to="{ path: '/mainTemp/wallet/deposit/crypto' }"
              exact-active-class="router-link-actived"
            >
              واریز
            </nuxt-link>
          </div>
          <div class="subItems">
            <nuxt-link to="#"> برداشت </nuxt-link>
          </div>
          <div class="subItems">
            <nuxt-link to="#"> تاریخچه واریز و برداشت </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      current: 1,
      accardeon: false,
    };
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
.rightContent {
  width: 15%;
  height: 850px;
  box-shadow: rgba(0, 0, 0, 0.08) 0px 2px 4px, rgba(0, 0, 0, 0.08) 0px 0px 2px;
  // background-color: dod;
  float: right;
  .items {
    width: 100%;
    height: auto;
    // float: left;
    .title {
      text-align: right;
      color: #ffffff;
      font-family: yekan, sans-serif;
      font-size: 16px;
      padding: 15px 10px;
      width: 100%;
      span {
        color: rgb(33, 40, 51);
        font-weight: 400;
        font-size: 14px;
      }
      svg {
        vertical-align: middle;
        margin-right: 9px;
        margin-left: 5px;
        float: right;
        fill: rgb(132, 142, 156);
        color: rgb(132, 142, 156);
      }
      .down {
        float: left;
        margin-left: 10px;
        font-size: 10px;
        margin-top: 5px;
        color: rgb(132, 142, 156);
      }
      .up {
        float: left;
        margin-left: 10px;
        font-size: 10px;
        margin-top: 8px;
        color: rgb(132, 142, 156);
      }
      &:hover {
        background-color: #76808f15;
      }
    }
    .subMenus {
      width: 100%;
      max-height: 0;
      overflow: hidden;
      //   background-color: dodgerblue;
      transition: max-height 0.4s ease-in;
      .subItems {
        // direction: rtl;
        a {
          width: 100%;
          height: 48px;
          display: block;
          // background-color: rgb(18, 22, 28);
          color: rgb(33, 40, 51);
          font-weight: 400;
          font-size: 14px;
          text-align: right;
          // float: right;
          text-decoration: none;
          font-family: yekan, sans-serif;
          padding-right: 44px;
          line-height: 48px;
          white-space: nowrap;
          border-right: 4px solid transparent;
          &:hover {
            background-color: #76808f15;
          }
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
.router-link-actived {
  border-right: 4px solid rgb(240, 185, 11) !important;
  background-color: #76808f15;
  font-weight: bold!important;
}
@media only screen and (max-width: 1240px) {
  .rightContent{
    width: 20%;
  }

 
}
@media only screen and (max-width: 900px) {
  .rightContent{
    width: 24%;
  }

  
}

</style>