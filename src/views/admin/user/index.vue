<template>
<div class='user'>
  <div @click="handleClick" v-bind:class="[isActive ? activeClass : '', errorClass]">1111112311111</div>
  <div @click="handleTest">test</div>
  <div class='box'>
    <div class='animation' ref="p" >
      <div class='img1'>1</div>
      <div class='img1'>2</div>
      <div class='img1'>3</div>
      <div class='img1'>4</div>
    </div>
  </div>
</div>

</template>
<script>
export default {
  data() {
    return {
      isActive:true,
      activeClass:'height224',
      errorClass:'line'
    
    };
  },
  // 创建完毕
  mounted() {
//    windowAddMouseWheel();
// function windowAddMouseWheel() {
//     var scrollFunc = function (e) {
//         e = e || window.event;
//         console.log('滚动')
//         // if (e.wheelDelta) {  //判断浏览器IE，谷歌滑轮事件
//         //     if (e.wheelDelta > 0) { //当滑轮向上滚动时
//         //         alert("滑轮向上滚动");
//         //     }
//         //     if (e.wheelDelta < 0) { //当滑轮向下滚动时
//         //         alert("滑轮向下滚动");
//         //     }
//         // } else if (e.detail) {  //Firefox滑轮事件
//         //     if (e.detail> 0) { //当滑轮向上滚动时
//         //         alert("滑轮向上滚动");
//         //     }
//         //     if (e.detail< 0) { //当滑轮向下滚动时
//         //         alert("滑轮向下滚动");
//         //     }
//         // }
//     };
//     //给页面绑定滑轮滚动事件
//     if (document.addEventListener) {
//         document.addEventListener('scroll', scrollFunc, false);
//     }
// //滚动滑轮触发scrollFunc方法
//     window.onmousewheel = document.onmousewheel = scrollFunc;
// }
  },
   methods: {
     handleClick() {
       this.isActive = !this.isActive
     },
     handleTest() {
       console.log('',)
       this.$refs.p.style.transform='translateX(600px)'
     }
  }
  // 即将更新渲染
  // beforeUpdate() {
  //   this.importFontpack("admin/user/");
  // },
  
};
</script>
<style>
.user{
  position: relative;
}
 ul {
      width: 400px;
      overflow: hidden;
      display: flex;
    }
    li{
      width: 400px;
      list-style-type:none;
      flex-shrink: 0;
    }
  .line {
    margin-left: 20px;
    border: 1px solid #E3ECF1;
    height: 56px;
    width: 0px;
    margin: 12px 0;
    transition: height 0.3s;

  }

  .height136 {
    height: 136px
  }

  .height224 {
    height: 224px
  }

   @keyframes wordsLoop {
      0% {
        transform: translateX(600px);
      }

      100% {
        transform: translateX(-100%);
      }
    }

    .box {
      width: 600px;
      overflow: hidden;
      position: relative;
      margin-right: 26px;
    }
    .animation {
      display: flex;
      padding-left: 20px;
      color: #FF0027;
      font-size: 24px;
      line-height: 24px;
      white-space: nowrap;
      /* animation: wordsLoop 10s linear infinite normal; */

    }
    .img1 {
      width:600px;
      flex-shrink: 0;
    }
</style>