<template>
  <div>
    <div class="depositTitle"><p>واریز</p></div>
    <div class="depositNavs">
      <nuxt-link
        :to="{ path: '/mainTemp/wallet/deposit/crypto' }"
        exact-active-class="router-link-actived"
      >
        کریپتو
      </nuxt-link>
      <nuxt-link to="#"> فیات </nuxt-link>
    </div>

    <div class="cryptoContent">
      <div class="cryptoRightPart">
        <span>کریپتو</span>
        <div class="cryptoSelect">
          <i class="fas fa-angle-down"></i>
          <select v-model="selected">
            <option
              v-for="(option, i) in options"
              :key="i"
              v-bind:value="option.value"
            >
              {{ option.text }}
            </option>
          </select>
        </div>
        <div class="cryptoMojody">
          <div class="mojItems">
            <span> موجودی کل:</span>
            <span> BTC:۰.۰۰۰۰۰۰۰۰ </span>
          </div>
          <div class="mojItems">
            <span> در درخواست:</span>
            <span>BTC:۰.۰۰۰۰۰۰۰۰ </span>
          </div>
          <div class="mojItems">
            <span>موجودی شما:</span>
            <span>BTC:۰.۰۰۰۰۰۰۰۰ </span>
          </div>
        </div>
      </div>
      <div class="cryptoLeftPart"></div>
    </div>
    <div class="lstTenPay" dir="rtl">
      <p>۱۰ واریز اخیر شما</p>

      <div class="payTable">
        <table>
          <thead>
            <tr>
              <th>نوع رمز ارز</th>
              <th>تاریخ</th>
              <th>مقدار</th>
              <th>کد</th>
              <th>وضعیت</th>
              <th>اطلاعات</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td colspan="6">
                <span>اطلاعاتی پیدا نشد</span>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selected: "ETH",
      options: [
        { text: "BTC", value: "BTC" },
        { text: "ETH", value: "ETH" },
        { text: "UDTC", value: "UDTC" },
      ],
    };
  },
};
</script>
<style lang="less" scoped>
.depositNavs {
  width: 94%;
  height: 40px;
  margin: 0 auto;
  clear: both;
  border-bottom: 1px solid rgb(230, 232, 234);
  a {
    text-decoration: none;
    color: rgb(118, 128, 143);
    font-family: yekan, sans-serif;
    float: right;
    font-weight: 700;
    font-size: 16px;
    line-height: 40px;
    height: 100%;
    margin-left: 30px;
  }
}
.depositTitle {
  display: block;
  width: 100%;
  height: auto;
  clear: both;
  p {
    float: right;
    font-family: yekan, sans-serif;
    color: black;
    font-size: 34px;
    font-weight: bold;
    padding: 20px 30px;
    margin: 0;
  }
}

.cryptoContent {
  width: 94%;
  margin: 40px auto;
  height: auto;
 
  .cryptoRightPart {
    width: 50%;
    height: 100%;
    float: right;
    padding-bottom: 150px;
    span {
      color: rgb(33, 40, 51);
      font-size: 12px;
      float: right;
    }
    .cryptoSelect {
      width: 100%;
      height: 40px;
      margin-top: 15px;
      float: right;
      clear: both;
      position: relative;
      select {
        width: 100%;
        height: 100%;
        background-color: transparent;
        border: 1px solid rgb(230, 232, 234);
        border-radius: 3px;
        direction: rtl;
        appearance: none;
        -webkit-appearance: none;
        -moz-appearance: none;
        outline-color: rgb(230, 232, 234);
        padding-right: 20px;
      }
      i {
        vertical-align: middle;
        position: absolute;
        top: 12px;
        left: 10px;
        color: rgba(0, 255, 255, 0.582);
      }
    }
    .cryptoMojody {
      direction: rtl;
      width: 94%;
      height: auto;
      padding-top: 30px;
      clear: both;
      float: right;
      .mojItems {
        width:100%;
        height: 30px;
        float: right;
        span:first-child {
              display: inline-block;
    min-width: 130px;
          color: rgb(146, 154, 165);
          font-weight: 400;
          font-size: 14px;
          font-family: yekan, sans-serif;

        }
        span:last-child {
          color: rgb(33, 40, 51);
          font-size: 14px;
          float: right;
          font-weight: bold;
          font-family: yekan;
        }
      }
    }
  }
}
.lstTenPay {
  width: 94%;
  height: auto;
  margin: 50px auto;
  overflow-x: auto;
  white-space: nowrap;
  border-top: 1px solid #e6e8ea;
  .payTable {
    clear: both;

    height: 200px;
    table {
      width: 100%;
      padding: 0 2px 5px;
      display: table;
      text-align: right;
      border-radius: 2px 2px 0 0;
      //   border-collapse: separate;
      border-spacing: 0;
      thead {
        background-color: #9ec3e6;

        tr {
          th {
            vertical-align: middle;
            width: 50px;
            padding: 15px 15px;
            // line-height: 10px;
            color: #848e9c !important;
            font-size: 12px !important;
            font-weight: 400 !important;
            background-color: #f9f9fa;
            border-bottom: none !important;
          }
        }
      }
      span {
        color: #76808f;
        min-width: 320px;
        font-weight: 400;
        font-size: 14px;
        text-align: center;
        display: block;
        margin-top: 50px;
      }
    }
  }
  p {
    float: right;
    font-family: yekan, sans-serif;
    color: rgb(30, 32, 38);
    font-size: 24px;
    font-weight: 700;
    margin-top: 25px;
  }
}
.router-link-actived {
  color: rgb(30, 32, 38) !important;
  border-bottom: 2px solid rgb(240, 185, 11);
}
@media only screen and (max-width: 766px) {
  .cryptoRightPart {
    width: 100%!important;
  }
//   .leftContent {
//     width: 100%;
//   }
}
</style>

