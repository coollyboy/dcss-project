<template>
    <div class="indexbox">
        <div class="guntxt">
            <ul class="ullist">
                <li v-for="(item, index) in list" :key="index">
                    <img class="name" :src="item.src" alt="">
                </li>
            </ul>
        </div>
        <div class="aboutme">
            <li class="listyle1">Who We Are And Can Do For Your</li>
            <li class="listyle3">
                北京鼎成盛世广告策划有限公司是集于广告、公关活动、企业策划、庆典策划、
                会议会展与执行的综合型企业，总部坐落于北京本土通州北关绿地大厦，鼎成
                从事该行业近十年，有着丰富的经验、优秀的团队、先进的设备、创新的理念，
                项目覆盖全国多个省市如北京、河北、河南、东北、四川、浙江、云南、西藏、
                新疆等多地区。北京鼎成盛世广告策划有限公司：注册资金200万，员工16人，
                拥有一支金牌创意团队，面向全国，为各企业提供高端全定制企业服务，满足
                各企业对品牌建设及推广的个性化需求。
            </li>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            list:[
                {src:require('../assets/img/a1.png')},
                {src:require('../assets/img/a2.png')},
                {src:require('../assets/img/a3.png')},
                {src:require('../assets/img/a4.png')},
                {src:require('../assets/img/a5.png')},
                {src:require('../assets/img/a1.png')},
            ],
        }
    },
    methods: {
        
    },
}
</script>
<style lang="less" scoped>
@media only screen and (min-width: 751px) {
    .indexbox{
        width:100%;
        min-height: 100%;
        margin-top:100px;
        .guntxt{
            width: 80%;
            height: 550px;
            margin:0 auto;
            overflow: hidden;
            background: #ffffff;
            position: relative;
            top:2px;
        }
        .ullist{
            animation: myMove 20s linear infinite;
            animation-fill-mode: forwards;
            li{
                height: 550px;
                width:100%;
                .name{
                    width:100%;
                    height: 550px;
                    -webkit-background-size:cover;
                    -moz-background-size: cover;
                    -o-background-size: cover;
                    background-size: cover;
                }
            }
        }
        @keyframes myMove {
            0% {
                transform: translateY(0);
            }
            100% {
                transform: translateY(-2750px);
            }
        }
        .aboutme{
            margin-top:100px;
            width:cale( 100% - 100px );
            height: 350px;
            background: #e7f6ff;
            padding:50px;
            .listyle1{
                width:100%;
                height: 100px;
                font-size:50px;
                font-weight: 700;
                color:white;
            }
            .listyle3{
                width:100%;
                height: 150px;
                line-height: 50px;
                font-size: 28px;
                text-indent: 50px;
                font-weight: 500;
            }
        }
    }
}
@media only screen and (max-width: 750px) {
    .indexbox{
        width:100%;
        min-height: 100%;
        margin-top:100px;
        .guntxt{
            width: 80%;
            height: 350px;
            margin:0 auto;
            overflow: hidden;
            background: #ffffff;
            position: relative;
            top:50px;
        }
        .ullist{
            animation: myMove 20s linear infinite;
            animation-fill-mode: forwards;
            li{
                height: 350px;
                width:100%;
                .name{
                    width:100%;
                    height: 350px;
                    -webkit-background-size:cover;
                    -moz-background-size: cover;
                    -o-background-size: cover;
                    background-size: cover;
                }
            }
        }
        @keyframes myMove {
            0% {
                transform: translateY(0);
            }
            100% {
                transform: translateY(-1750px);
            }
        }
        .aboutme{
            margin-top:100px;
            width:cale( 100% - 100px );
            min-height: 350px;
            background: #e7f6ff;
            padding:30px;
            .listyle1{
                width:100%;
                min-height: 100px;
                font-size:30px;
                font-weight: 700;
                color:white;
            }
            .listyle3{
                width:100%;
                min-height: 150px;
                line-height: 30px;
                font-size: 18px;
                text-indent: 50px;
                font-weight: 500;
            }
        }
    }
}
</style>