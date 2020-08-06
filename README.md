## 环境依赖
composer 依赖
```shell
"overtrue/wechat": "~4.2.30"
php 7.x
```

## 部署步骤

在本地模块进行安装 确保Install目录存在

## 目录结构描述
```shell
D:.
│  Config.inc.php   模块配置配置简介
│  README.md
│
├─Controller
│      AuthController.class.php  登录授权功能
│      IndexController.class.php  获取jssdk
│      MiniController.class.php   小程序基础功能
│      MiniLiveController.class.php   小程序直播功能
│      MiniSubscribeMessageController.class.php  小程序订阅消息
│      OfficeController.class.php  公众号基础功能
│      ServerController.class.php  消息接收处理
│      WechatController.class.php  微信(公众号+小程序)管理
│      WxpayController.class.php  微信(公众号+小程序)支付、退款、企业到付等
│      WxpayNotifyController.class.php 微信支付回调
│
├─CronScript
│      HandleWxpay.class.php 定时任务
│
├─Install
│      Menu.php 安装菜单
│      Wechat.sql 安装表
│
├─Model 调用的Model信息
│      AutoTokenModel.class.php  用户登录凭证
│      MiniCodeModel.class.php  小程序码
│      MiniLiveModel.class.php  小程序直播
│      MiniFormIdModel.class.php  模板消息form_id
│      MiniPhoneNumberModel.class.php  获取小程序手机号
│      MiniSendMessageRecordModel.class.php  小程序订阅消息发送记录
│      MiniSubscribeMessageModel.class.php  小程序订阅消息
│      MiniTemplateListModel.class.php  小程序模板消息列表
│      MiniUsersModel.class.php  小程序用户信息
│      OfficeEventMessageModel.class.php  公众号消息通知事件
│      OfficeMediaModel.class.php  公众号消息
│      OfficeMessageModel.class.php  公众号消息模板
│      OfficeQrcodeModel.class.php  公众号参数二维码
│      OfficeSendTemplateRecordModel.class.php  公众号消息模板发送记录
│      OfficesModel.class.php  微信(公众号+小程序)资料
│      OfficeTemplateListModel.class.php  公众号消息模板列表
│      OfficeUsersModel.class.php  公众号用户信息
│      WxpayMchpayModel.class.php  公众号
│      WxpayOrderModel.class.php  微信(公众号+小程序)支付
│      WxpayRedpackModel.class.php  微信(公众号+小程序)企业到付
│      WxpayRefundModel.class.php  微信(公众号+小程序)退款
│
├─Service
│      MiniCodeService.class.php  小程序二维码
│      MiniLiveService.class.php  小程序直播
│      MiniService.class.php  小程序公共文件
│      MiniSubscribeMessageService.class.php 小程序订阅消息
│      MiniTemplateService.class.php  小程模板消息
│      MiniUsersService.class.php 小程序用户信息
│      OfficeQrcodeService.class.php  公众号二维码
│      OfficeService.class.php 公众号公共文件
│      OfficeTemplateService.class.php 公众号事件消息
│      WxpayService.class.php 微信(公众号+小程序)支付，退款，企业到付功能
│
├─Uninstall
│      Wechat.sql 卸载模块
│
└─View 页面
    ├─Mini
    │      codelist.php  小程序码列表
    │      templatelist.php 小程序消息模板列表
    │      users.php 小程序用户列表
    │
    ├─MiniSubscribeMessage
    │      lists.php 小程序消息模板列表
    │      sendMessageRecordList.php 订阅消息发送日志
    │      testSend.php 小程序消息模板详情
    │
    ├─MiniLive
    │      lists.php 小程序直播列表
    │
    ├─Office
    │  │  eventmessagelist.php 公众号事件消息列表
    │  │  messagelist.php 公众号消息列表
    │  │  qrcodelist.php 公众号参数二维码列表
    │  │  templatelist.php 公众号消息模板列表
    │  │  users.php 公众号 公众号用户列表
    │  │
    │  └─MessageType
    │          content.php  文本消息
    │          image.php  图片消息
    │          link.php  链接消息  
    │          location.php  位置消息
    │          video.php  视频消息
    │          voice.php  音频消息
    │
    ├─Wechat
    │      editOffice.php  添加或者微信(公众号+小程序)基本信息
    │      index.php 微信(公众号+小程序)基本信息管理
    │
    └─Wxpay
            mchpays.php  企业付款
            orders.php   支付订单
            redpacks.php 退款订单
            refunds.php 发送红包
```

##版本内容更新


##### 版本号 ： 1.0.0.0 （2020年8月4日）

功能  | 介绍  
 ---- | ----- 
 初始化项目  | 完善项目的文档说明，添加基本的目录结构介绍 
 
<br> 
<br> 

##### 版本号 ： 1.1.0.0 （2020年8月5日）

功能  | 介绍  
 ---- | ----- 
 小程序直播  | 提供直播，直播回放功能
