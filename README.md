# photp-preview
**简介**
该插件是基于photoswipe.js，仿照vue-photo-preview的，因为vue-photo-preview没有单击关闭的方法，因此我在此基础上进行了修改，将单击关闭、是否显示放大图标、是否显示分享、是否显示关闭按钮等功能对外有用户自定义

**不足**
暂不支持多张图片放大展示及滑动切换，因为是移动端多张图片可能是以轮播图的形式展示也可能是以九宫格的形式进行展示，后期会对其进行扩展补充

**使用**
npm install photp-preview --save-dev

```javascript
<template>
    <div class = "demo">
        <photo class = "img"
               :imgs = "src"
               :shareEl = false // 是否显示分享按钮
               :tapToClose = false // 是否支持单击关闭
               :zoomEl = false // 是否显示放大按钮
               :closeEl = false // 是否显示关闭按钮
        ></photo>
    </div>
</template>
<script>
    import photo from 'photp-preview' //文件引入
    export default {
        name: "demo",
        components:{photo}, //注入
        data(){
            return{
                src: 'https://farm2.staticflickr.com/1043/5186867718_06b2e9e551_b.jpg'
            }
        }
    }
</script>

<style  lang="less" scoped="scoped">
    .demo{
        .img{
            width:100%;
            height:300px;
            padding:20px;
        }
    }
</style>
```
