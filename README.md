### uni-app开发的新闻/资讯类App，一套代码可编译到iOS、Android、H5、以及各种小程序等多个平台。

### 网络请求、模板语法、打开页面、页面传参

## 列表到详情接口

### 列表
https://unidemo.dcloud.net.cn/api/news
- 返回数据格式
- post_id 新闻id 如 ： 72980
- title 标题
- created_at 创建时间
- author_avatar 图标

### 详情

地址：https://unidemo.dcloud.net.cn/api/news/36kr/ + id（id为新闻id，上个页面传过来的）

使用 rich-text 【富文本组件】来展示新闻内容
<rich-text class="richText" :nodes="strings"></rich-text>

```
condition
启动模式配置，仅开发期间生效，用于模拟直达页面的场景，如：小程序转发后，用户点击所打开的页面。

"condition": { //模式配置，仅开发期间生效
    "current": 0, //当前激活的模式（list 的索引项）
    "list": [{
            "name": "swiper", //模式名称
            "path": "pages/component/swiper/swiper", //启动页面，必选
            "query": "interval=4000&autoplay=false" //启动参数，在页面的onLoad函数里面得到。
        },
        {
            "name": "test",
            "path": "pages/component/switch/switch"
        }
    ]
}

```


