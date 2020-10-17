<template>
  <div>
    <div class="acardeonFooter">
      <div class="acardeonItems">
        <div class="title" @click="acr(1)">
          <span>درباره ما</span>
          <i class="fas fa-plus"></i>
        </div>
        <div class="subAcardeon" :class="{ active: current == 1 }">
          <nuxt-link to="#">درباره ما</nuxt-link>
          <nuxt-link to="#">مقررات و حریم خصوصی</nuxt-link>
          <nuxt-link to="#">بلاگ</nuxt-link>
        </div>
      </div>
      <div class="acardeonItems">
        <div class="title" @click="acr(2)">
          <span> پشتیبانی</span>
          <i class="fas fa-plus"></i>
        </div>
        <div class="subAcardeon" :class="{ active: current == 2 }">
          <nuxt-link to="#"> سوالات متداول</nuxt-link>
          <nuxt-link to="#"> کارمزدها </nuxt-link>
        </div>
      </div>
      <div class="acardeonItems">
        <div class="title" @click="acr(3)">
          <span> ارتباط با ما</span>
          <i class="fas fa-plus"></i>
        </div>
        <div class="subAcardeon" :class="{ active: current == 3 }">
          <div>
            <p class="connectP">
              ۲۴ پشتیبانی هر روز از ۸.۳۰ تا

              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="15"
                height="15"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
                class="icon phone"
              >
                <path
                  d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"
                ></path>
              </svg>
            </p>
            <p class="connectPs">۰۲۱-۹۱۰۱۲۳۰۰</p>
          </div>
          <div>
            <p class="connectP">
              ایمیل پشتیبانی
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="15"
                height="15"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
                class="icon mail"
              >
                <path
                  d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"
                ></path>
                <polyline points="22,6 12,13 2,6"></polyline>
              </svg>
            </p>
            <p class="connectPs">support@mrbitex.com</p>
          </div>
          <div>
            <p class="connectP">
              ایمیل روابط عمومی

              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="15"
                height="15"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
                class="icon mail"
              >
                <path
                  d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"
                ></path>
                <polyline points="22,6 12,13 2,6"></polyline>
              </svg>
            </p>
            <p class="connectPs">info@mrbitex.com</p>
          </div>
        </div>
      </div>
      <div class="acardeonItems">
        <div class="title" @click="acr(4)">
          <span> شبکه های اجتماعی</span>
          <i class="fas fa-plus"></i>
        </div>
        <div class="subAcardeon" dir="rtl" :class="{ active: current == 4 }">
          <nuxt-link class="social" to="#"
            ><svg
              xmlns="http://www.w3.org/2000/svg"
              width="18"
              height="18"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="icon instagram"
            >
              <rect x="2" y="2" width="20" height="20" rx="5" ry="5"></rect>
              <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"></path>
              <line x1="17.5" y1="6.5" x2="17.51" y2="6.5"></line></svg
          ></nuxt-link>
          <nuxt-link class="social" to="#">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="18"
              height="18"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="icon twitter"
            >
              <path
                d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"
              ></path>
            </svg>
          </nuxt-link>
          <nuxt-link class="social" to="#">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="18"
              height="18"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="icon send"
            >
              <line x1="22" y1="2" x2="11" y2="13"></line>
              <polygon points="22 2 15 22 11 13 2 9 22 2"></polygon>
            </svg>
          </nuxt-link>
          <nuxt-link class="social" to="#">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="18"
              height="18"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="icon linkedin"
            >
              <path
                d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"
              ></path>
              <rect x="2" y="9" width="4" height="12"></rect>
              <circle cx="4" cy="4" r="2"></circle>
            </svg>
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      current: "",
    };
  },
  methods: {
    acr(val) {
      if (this.current == val) {
        this.current = "";
      } else {
        this.current = val;
      }
    },
  },
};
</script>

<style lang="less" scoped>
.acardeonFooter {
  //   padding: 0 30px 0 30px;
  height: auto;
  .acardeonItems {
    border-bottom: 1px solid #ffffff23;

    .title {
      padding: 0 15px 0 15px;
      width: 95%;
      margin: 0 auto;
      height: 60px;
cursor: pointer;
      span {
        font-size: 20px;
        font-family: yekan, sans-serif;
        font-weight: 500;
        color: #ffffff;
        float: right;
        line-height: 60px;
      }
      i {
        color: #ffffff;
        font-size: 10px;
        line-height: 60px;
      }
    }
    .subAcardeon {
      width: 95%;
      height: 0;
      overflow: hidden;
      margin: 0 auto;
      padding: 0 15px 0 15px;
      a {
        display: block;
        text-align: right;
        text-decoration: none;
        margin-bottom: 10px;
        font-size: 14px;
        font-family: yekan, sans-serif;
        font-weight: 400;
        color: rgb(118, 128, 143) !important;
        &:hover {
          color: #ffffff !important;
        }
      }
      .social {
        text-align: right;
        display: inline-block;
        padding-left: 30px;
        // direction: ltr;
      }
      div {
        clear: both;
        margin-bottom: 10px;
        .connectP {
          color: rgb(118, 128, 143) !important;
          display: block;
          text-align: right;
          margin: 0;
          padding: 0;
          font-family: yekan, sans-serif;
          //   float: right;
          svg {
            text-align: right;
            display: block;
            float: right;
            margin-top: 5px;
            margin-left: 5px;
          }
        }
        .connectPs {
          margin-right: 20px;
          font-family: yekan, sans-serif;
          direction: rtl;
          color: rgb(118, 128, 143) !important;
          display: block;
        }
      }
    }
  }
}
.active {
  height: auto !important;
}
@media only screen and (min-width: 840px) {
  .acardeonFooter{
      display:none;
  }
}
</style>