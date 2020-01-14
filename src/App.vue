<template>
  <div id="app">
    <div class="mainlist">
        <div class="mainleft">
            {{name}}
        </div>
        <div class="mainright">
            <li class="listyle" :class="{colorble:colorselect==index}" v-for="(item,index) in itemlist" @click="toselect(index)" :key="index">{{item.text}}</li>
        </div>
    </div>
    <router-view/>
    <div class="footer">
        <span @click="togongxinbu">京ICP备19048406号-1</span>
    </div>
  </div>
</template>
<script>
export default {
    data() {
        return {
            name:'鼎成盛世',
            colorselect:0,
            itemlist:[
                {text:'首页'},
                {text:'关于我们'},
                {text:'服务项目'},
                {text:'经典案例'},
                {text:'活动策划'},
                {text:'行业资讯'},
                {text:'联系我们'},
            ]
        }
    },
    methods: {
        toselect(index){
            this.colorselect = index
        },
        togongxinbu(){
            window.location.href='http://beian.miit.gov.cn'
        }
    },
}
</script>
<style lang="less" scoped>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
//   text-align: center;
  color: #2c3e50;
}
.mainlist{
    width:100%;
    height: 100px;
    background-color:#f0ffff;
    position: fixed;
    top:0;
    left:0;
    right:0;
    overflow: hidden;
    z-index: 9999;
    .mainleft{
        width:30%;
        height: 100px;
        line-height: 100px;
        text-align: center;
        font-size:40px;
        font-weight: 700;
        color:#4dd3d2;
        float: left;
    }
    .mainright{
        float: right;
        width:70%;
        height: 100px;
        overflow: hidden;
        .listyle{
            width:100px;
            height: 30px;
            line-height: 30px;
            float: left;
            text-align: center;
            font-size:20px;
            list-style: none;
            // border:red 1px solid;
            margin-right:20px;
            margin-top:35px;
        }
        .colorble{
            background-color: #4dd3d2;
            border-radius: 10px;
            // color: blue;
        }
    }
}
.footer{
    margin-top:10px;
    width:100%;
    height: 80px;
    line-height: 80px;
    text-align: center;
    font-size: 20px;
    color:#545454;
}
</style>
