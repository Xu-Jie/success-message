<template>
  
      <!-- 全局提示框 -->
      <div v-show="visible" class="dialog-tips dialog-center">
          <img src="@/assets/img/icon/u396.png" alt="">
          <div>{{message}}</div>
      </div>
  
</template>
<script>
export default {
  data() {
    return {
      visible: false,
      message: ""
    };
  }
};
</script>
<style lang="scss" scoped>
.dialog-tips{
    position: fixed;
    z-index: 9998;
    min-width: 150px;
    padding: 15px 22px;
    white-space: nowrap;
    background-color: #fff;
    box-shadow: 0px 8px 15px 0 rgba(0, 0, 0, 0.1);
    text-align: center;
    .dialog-tips-icon{
        width: 54px;
        height: 54px;
        // @extend %bg-contain;
        display: inline-block;
        margin-bottom: 13px;
    }
    img{
        float: left;
        margin:3px 10px;
        margin-left: 40px;
    }
    div{
        float: left;
    }
}
.dialog-center {
    top: 10%;
    left: 50%;
    transform: translate(-60%, -50%);
    transition: transform .5s;
}
.animate{
    transform: translate(-50%, -50%);
    transition: transform .5s;
}

</style>