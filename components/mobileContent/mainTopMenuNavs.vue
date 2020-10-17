<template>
  <div>
    <div class="mainTopMobileNavs">
      <div class="topPart">
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
        <p>کیف پول</p>
      </div>
      <div class="bottomPart">
        <ul>
          <li>
            <nuxt-link to="#">موجودی </nuxt-link>
          </li>
          <li>
            <nuxt-link :to="{path:'/mainTemp/wallet/deposit/crypto'}" exact-active-class="router-link-actived">واریز </nuxt-link>
          </li>
          <li>
            <nuxt-link to="#">برداشت </nuxt-link>
          </li>
          <li>
            <nuxt-link to="#">تاریخچه واریز و برداشت </nuxt-link>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style lang="less" scoped>
.mainTopMobileNavs {
  width: 100%;
  //   height: 200px;
  display: block;
  background-color: #12161c;

  display: block;
  .topPart {
    width: 100%;
    height: 30px;
    // background-color: cyan;
    svg {
      float: right;
      color: rgb(240, 185, 11);
      fill: rgb(240, 185, 11);
      margin-right: 20px;
      margin-left: 3px;
    }
    p {
      color: #fff;
      font-family: yekan, sans-serif;
      text-align: right;
      font-size: 16px;
      float: right;
      // direction: rtl;
      font-weight: bold;
      // display: inline-block;
      border-bottom: 2px solid rgb(240, 185, 11);
    }
  }
  .bottomPart {
    width: 100%;
    height: 50px;
    // background-color: darkorchid;
    ul {
      list-style-type: none;
      direction: rtl;
      padding: 0 15px 0 0;
      li {
        display: inline-block;
        line-height: 50px;
        margin-left: 10px;
        a {
          text-decoration: none;
          color: #ffffff;
          font-family: yekan, sans-serif;
        }
      }
    }
  }
}
.router-link-actived{
  font-weight: bold;
}
</style>