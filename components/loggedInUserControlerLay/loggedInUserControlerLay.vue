<template>
  <div>
    <div class="loggedInController">
      <a href="#" class="seprator">
        <i class="fas fa-angle-left"></i>
        forexapmle@gmail.com
      </a>
      <a href="#">
        <svg
          aria-hidden="true"
          focusable="false"
          fill=" rgb(132, 142, 156)"
          width="18"
          height="18"
          class="icon security"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 1024 1024"
        >
          <path
            d="M170.666667 213.333333h682.666666v408.746667l-341.333333 195.072-341.333333-195.072V213.333333z m85.333333 85.333334v273.92l256 146.261333 256-146.261333V298.666667H256z"
          ></path>
        </svg>

        امنیت
      </a>
      <a href="#" class="seprator">
        <svg
          aria-hidden="true"
          fill=" rgb(132, 142, 156)"
          focusable="false"
          width="18"
          height="18"
          class="icon id"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 1024 1024"
        >
          <path
            d="M743.850667 571.306667h-167.509334v78.848h167.509334V571.306667zM743.850667 413.653333h-167.509334v78.848h167.509334V413.653333zM416.426667 393.941333c35.114667 0 62.421333 27.605333 62.421333 63.061334 0 35.498667-27.306667 59.136-62.421333 63.061333-35.114667 3.968-62.421333-27.562667-62.421334-63.061333 0-35.456 27.306667-63.061333 62.421334-63.061334z m85.802666 256.213334H326.698667V571.306667h175.530666v78.848z"
          ></path>
          <path
            d="M170.666667 256v543.914667h725.333333V256H170.666667z m651.221333 465.066667H248.704V334.890667H817.92V721.066667h3.925333z"
          ></path>
        </svg>
        تایید هویت
      </a>
      <a href="#" class="seprator">
        <svg
          aria-hidden="true"
          fill=" rgb(132, 142, 156)"
          focusable="false"
          width="18"
          height="18"
          class="icon logout"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 1024 1024"
        >
          <path
            d="M535.893333 170.666667h-89.216v361.173333h89.173334V170.666667z"
          ></path>
          <path
            d="M490.837333 853.333333C313.344 852.906667 170.24 708.437333 170.666667 530.517333a321.194667 321.194667 0 0 1 93.653333-225.621333L327.168 368.213333a231.296 231.296 0 0 0 0.426667 327.722667 231.296 231.296 0 0 0 327.765333-0.426667 231.68 231.68 0 0 0 0-327.765333l62.890667-63.317333a321.706667 321.706667 0 0 1-0.896 454.826666A319.146667 319.146667 0 0 1 490.794667 853.333333z"
          ></path>
        </svg>
        خروج
      </a>
    </div>
  </div>
</template>

<script>
export default {};
</script>


<style lang="less" scoped>
.loggedInController {
  position: absolute;
  top: 100%;
  left: -5px;
  z-index: 999;
  width: 200px;
  height: auto;
  background-color: rgb(32, 34, 40);

  a {
    display: block;
    width: 100%;
    height: 55px;
    text-align: right;
    padding: 0 16px;
    font-family: yekan, sans-serif;
    font-weight: 400;
    color: #ffffff;
    text-decoration: none;
    // background-color: dodgerblue;
    margin: 0;
    float: right;
    line-height: 55px;
    i {
      float: left;
      line-height: 55px;
    }
    &:hover {
      color: #f0b90b;
      svg {
        fill: #f0b90b;
      }
    }
    svg {
      vertical-align: middle;
      margin-left: 5px;
    }
  }
}

.seprator {
  border-bottom: 1px solid rgba(247, 240, 240, 0.185);
}
</style>