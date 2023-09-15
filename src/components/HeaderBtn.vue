html
<template>
  <div class="header">
    <div class="image-container">
      <!-- 左 鄂电红马甲图标 -->
      <img class="img_left" :src="logo" alt="" title="鄂电红马甲" />

      <img :src="slogan" alt="" title="荆门东宝便民服务地图" class="img_center" />

      <div class="circle_btn">
        <img src="../assets/icon-selection.png" class="img_right" />
        <div class="search-list">
          <a v-for="(btn, index) in buttons" :key="index" :href="btn.href" class="button">{{ btn.label }}</a>
        </div>
      </div>
    </div>
    <div class="button-container">
      <a v-for="(btn, index) in buttons" :key="index" :href="btn.href" class="button">{{ btn.label }}</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      logo: require("../assets/logo.f5ffba99.png"),
      slogan: require("../assets/slogan.abb42670.png"),
      buttons: [
        { label: "电价政策", href: require("../assets/zhengche.jpg") },
        { label: "报装政策", href: require("../assets/baozhuang1.jpg") },
        { label: "综合能源服务", href: require("../assets/zonghe.jpg") }
      ]
    };
  }
};
</script>

<style type="text/css">
        body,
        html,
        #jingmen_map {
            width: 100%;
            height: 100%;
            overflow: hidden;
            margin: 0;
            font-family: "微软雅黑";
        }

        /* 清除默认边距 */
        * {
            margin: 0;
            padding: 0;
        }

        html {
            height: 100%;
        }

        a {
            text-decoration: none;
            color: #333;
        }

        .header {
            top: 0;
            left: 0;
            width: 100%;
            height: 125px;
            background: rgba(230, 242, 221, 0.95);
            display: flex;
            flex-direction: row;
            align-items: center;
            text-align: center;
            position: relative;
            justify-content: center;
        }

        .image-container {
            position: relative;
            display: flex;
            width: 100%;
            height: 48px;
            flex-direction: row;
            align-items: center;
            top: -26px;
            /* 添加一些间距 */
        }

        .image-class {
            position: fixed;
            right: 0;
            bottom: 0;
            width: 100px;   /*设置图片的宽度*/  
            height: 100px;  /*设置图片的高度*/ 
        }

        .button-container {
            width: 97%;
            height: 35px;
            padding: 0 10px;
            display: flex;
            align-items: center;
            background: hsla(0, 0%, 100%, 0.7);
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.04);
            backdrop-filter: blur(17px px);
            border-radius: 5px;
            overflow-x: auto;
            flex-direction: row;
            /* 让按钮并排显示 */
            justify-content: space-between;
            /* 在容器内均匀分布按钮 */
            position: absolute;
            /* 使按钮容器相对于 .header 定位 */
            bottom: 10px;
            /* 将小div的底部对齐设置为0 */
        }

        .button {
            display: flex;
            flex-grow: 1;
            padding: 0 8px;
            margin: 0px 3px;
            height: 22px;
            font-size: 12px;
            color: #000;
            line-height: 22px;
            text-align: center;
            text-decoration: none;
            white-space: nowrap;
            background: #fff;
            border: 1px solid #5bd162;
            box-shadow: 0 2px 5px #f5f5f5;
            border-radius: 24px;
            justify-content: center;
        }

        .img_center {
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            width: 216px;
            height: 51px;
        }

        .img_left {
            position: absolute;
            top: 5px;
            left: 16px;
            width: 36px;
        }

        .circle_btn {
            cursor: pointer;
            position: absolute;
            width: 48px;
            height: 48px;
            right: 15px;
            border-radius: 50%;
            /* 将外部div的边框半径设置为50%以创建圆形 */
            box-shadow: 0 4px 4px rgba(37, 136, 57, 0.2);
            justify-content: center;
            /* 水平居中 */
            align-items: center;
            /* 垂直居中 */
            overflow: hidden;
            /* 隐藏圆形外部div中超出的部分 */
            display: flex;
            background: #fff;
            transition: all 0.3s;
        }

        /* 鼠标边框变色 */
        .circle_btn:hover {
            box-shadow: 0 4px 4px rgba(37, 136, 57, 0.3);
        }

        .search-list {
            display: none;
            position: absolute;
            background-color: #f9f9f9;
            min-width: 160px;
            box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
            padding: 12px 16px;
        }

        .circle_btn:hover .search-list {
            margin-top: 100px;
            display: block;
        }

        .img_right {
            position: absolute;
            width: 40%;
            height: 40%;
        }

        .option {
            position: absolute;
            width: 100%;
            height: 20px;
            background: rgb(248, 251, 245);
        }

        body,
        html,
        #container {
            width: 100%;
            height: 100%;
            overflow: hidden;
            margin: 0;
            font-family: "微软雅黑";
        }

        .btn-wrap {
            z-index: 999;
            width: 100px;
            position: fixed;
            bottom: 30px;
            right: 10px;
            padding: 10px;
            border-radius: 5px;
            background-color: rgba(265, 265, 265, 0.9);
            box-shadow: 0 2px 6px 0 rgba(27, 142, 236, 0.5);
            display: flex;
            /* 使用 Flexbox 布局 */
            flex-direction: column;
            /* 纵向排列 */
            justify-content: center;
            /* 水平居中 */
            align-items: center;
            /* 垂直居中 */
        }

        .btn {
            width: 60px;
            height: 30px;
            float: left;
            background-color: #fff;
            color: rgba(27, 142, 236, 1);
            font-size: 14px;
            border: 1px solid rgba(27, 142, 236, 1);
            border-radius: 5px;
            margin: 5px 6px;
            text-align: center;
            line-height: 30px;
        }

        .btn:hover {
            background-color: rgba(27, 142, 236, 0.8);
            color: #fff;
            cursor: pointer;
        }

        ul li {
            list-style: none;
        }

        .tips {
            bottom: 16px;
            right: 4px;
            width: 120px;
        }

        .tel-btn {
            z-index: 999;
            bottom: 24px;
            left: 16px;
            width: 130px;
            display: flex;
            padding: 6px;
            align-items: center;
            color: #258839;
            font-size: 12px;
            line-height: 1;
            background: #fff;
            box-shadow: 0 0 4px rgba(0, 0, 0, 0.07);
            border-radius: 4px;
            font-size: 14px;
        }

        .tel-btn img {
            margin-right: 4px;
            width: 13px;
            height: 16px;
        }
</style>

<!-- <style scoped>
/* 在这里添加你的组件样式 */
.header {
    top: 0;
    left: 0;
    width: 100%;
    height: 125px;
    background: rgba(230, 242, 221, 0.95);
    display: flex;
    flex-direction: row;
    align-items: center;
    text-align: center;
    position: relative;
    justify-content: center;
}

.image-container {
    position: relative;
    display: flex;
    width: 100%;
    height: 48px;
    flex-direction: row;
    align-items: center;
    top: -26px;
    /* 添加一些间距 */
}

.image-class {
    position: fixed;
    right: 0;
    bottom: 0;
    width: 100px;   /*设置图片的宽度*/  
    height: 100px;  /*设置图片的高度*/ 
}

.button-container {
    width: 97%;
    height: 35px;
    padding: 0 10px;
    display: flex;
    align-items: center;
    background: hsla(0, 0%, 100%, 0.7);
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.04);
    backdrop-filter: blur(17px px);
    border-radius: 5px;
    overflow-x: auto;
    flex-direction: row;
    /* 让按钮并排显示 */
    justify-content: space-between;
    /* 在容器内均匀分布按钮 */
    position: absolute;
    /* 使按钮容器相对于 .header 定位 */
    bottom: 10px;
    /* 将小div的底部对齐设置为0 */
        }
</style> -->