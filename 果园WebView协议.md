# 果园 WebView 跳转协议

举例：

```
fruitday://path?parameter1=v1&parameter2=v2)
```

webUrl 转换规则：``# 替换 ?``,``* 替换 =``。

```
fruitday://LaunchMiniProgram?userName=gh_329d04d99224&path=/pages/webView/index#src*https://huodongcdnqn.fruitday.com/sale/foretaste_v2/index.html#id*85
```



协议名称 | 协议 Path | 入参 
:--|:--|:--
登陆						|Login				|none
分享						|Share 			|[FDShareCenterObject](#FDShareCenterObject)
跳转商品详情				|Product 			|productId,storeId
返回上一个原生页面			|Back 				|none
跳转购物车					|Cart 				| none
跳转我的礼品				|Gift 				|none
跳转礼品详情页				|GiftDetail 		|none
跳转我的优惠券				|Coupon 			| none
跳转订单详情页				|OrderComplete 	|orderName
跳转充值页					|TopUp				| none
商品加入购物车				|addToCartInH5	|productId
关闭首页 H5 弹窗			|closeRocketWebView | none
跳转联系客服				|ContactService	| none
跳转百科文章				|Guoshi_Baike		|target_id
跳转社区文章				|Guoshi_Shequ		|target_id
跳转社区活动				|Guoshi_Activity	|target_id
跳转我的积分				|CreditHistory	|none
跳转我的等级				|UserLevel		|none
跳转绑定手机				|BoundMobile		| none
跳转摇一摇记录				|ShakeHistory		|none
跳转商品搜索页				|Search			|searchKey
跳转分类列表页				|CategoryProductList |categoryId
唤起收银台					|CallCashierDesk	|orderName
关闭收银台					|CloseCashierDesk |none
跳转带导航条 H5				|h5withNav		|URL
跳转不带导航条 H5			|h5withNoNav		|URL
购买邮费 Vip 成功回调		|buyFreightVipSuccess |none
跳转 CityBox 扫码			|CityboxScan		|none
跳转杉德卡绑定页			|SandBinding		|none
复制文案					|Copy				|copyString
跳转杉德卡列表页			|GoToSandCard		|none
刷新购物车红点				|RefreshCartRedDot |none
跳转聊天客服页				|GoToChat			|none
拨打客服电话有弹窗			|GoToDial			|none
拨打电话无弹窗				|Tel				|phoneNo.
跳转菜谱列表				|CookbookList		| target_id
跳转菜谱首页				|CookbookHome		|none
跳转菜谱详情页				|CookbookDetail	| target_id
跳转提货券扫描页			|Tihuoquan		|none
提货券扫描成功				|TihuoquanSuccess |number,password
跳转充值页手动输入 Tab		|ChargeOffline	|none
启动小程序					|LaunchMiniProgram |userName,path
设置 iPhoneX 底部占位色	|SetBottomColor	|hexString,bottomHeight
跳转订单列表页				|OrderList		|none
返回首页					|BackToHome		|none
v6 会员开通成功				|openVipNotification |none


### FDShareCenterObject

字段名|用途|类型|备注
:--|:--|:--|:--
sharePlatformTypes	|分享平台	| String		| 多类型用逗号隔开如：``0,1,2,3,4`` 类型：``0-qq分享 1-qq空间 2-朋友圈 3-微信好友 4-微博 5-朋友圈图片 6-小程序``
shareTitle			|分享标题	| String		|-
shareText				|分享内容	| String		|-
shareImageUrl			|分享图片	| String		|-
shareUrl				|分享链接	| String		|-
shareType				|分享类型	| Int			| 1、图片 2、Web
webpageUrl			|兼容微信老版本	| String		| 仅启动小程序时需要
userName				|小程序wxID	| String		| 仅启动小程序时需要
path					|小程序路径	| String		| 仅启动小程序时需要