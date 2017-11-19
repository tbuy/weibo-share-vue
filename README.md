# weibo-vue

> vue集成新浪微博分享的demo，直接使用微博分享组件接口设置图标大小不起作用，如果自行对图标放大后非常模糊，所以写了这个demo。但是只对分享图标做了集成，之后会把分享按钮也做集成

## 安装

```
npm install
```
## 运行

```
npm run dev
```

## api

名称 | 类型 | 默认值 | 是否必选 | 描述
---|--- |--- |--- | ---
width | Number | 50 | no | 指定宽度(最大值50) 宽高1：1
appkey | Number | 无 | yes | 显示微博信息来源
text | String | 分享 | no | 分享的文字
pic | String | 无 | no | 图片的路径 多张图片通过"\|\|"分开

## 参考

[微博分享组件官方使用方法](http://jssdk.sinaapp.com/widget/share.php)

[微博分享按钮官方接口文档](http://jssdk.sinaapp.com/widget/share.php)
