# photp-preview
```javascript
<template>
    <div class = "demo">
        <photo class = "img"
               :imgs = "src"
               :shareEl = false
               :tapToClose = false
               :zoomEl = false
               :closeEl = false
        ></photo>
    </div>
</template>
<script>
    import photo from '../demo/photo'
    export default {
        name: "demo",
        components:{photo},
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
