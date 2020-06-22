<template>
  <div class="toast" v-if="flag" :class="{success: status=='success', fail: status=='fail',zhong:true,'fade-in':show, 'fade-out': !show}">
      <div v-if="status === 'success'" style="color: #4bad15 ">√ {{msg}}</div>
      <div v-if="status === 'fail'" style="color: #ec1b1b;">× {{msg}}</div>
  </div>
</template>

<script>
export default {

};
</script>

  <style>
  .zhong {
    text-decoration: underline;
  }
      .success {
          background: #a5fa73;
      }
      .fail {
          background: #f99;
      }
      .toast {
        position: fixed;
        top: 40px;
        left: 50%;
        transform: translateX(-50%);
        padding: 15px;
        border-radius: 3px;
      }
      .fade-in {
        animation: fadeIn 0.3s;
      }
      .fade-out {
        animation: fadeOut 0.3s;
      }

      @keyframes fadeIn {
        0% {
          top: 0;
          opacity: 0;
        }
        100% {
          top: 40px;
          opacity: 1;
        }
      }

      @keyframes fadeOut {
        100% {
          top: 0;
          opacity: 0;
        }
        0% {
          top: 40px;
          opacity: 1;
        }
      }
    </style>