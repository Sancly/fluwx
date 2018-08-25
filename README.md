![logo](/arts/fluwx_logo.png)

适用于Flutter的微信SDK，方便快捷。


## 使用需知
 使用```Fluwx```之前，强烈建议先阅读[微信SDK官方文档](https://open.weixin.qq.com/cgi-bin/showdocument?action=dir_list&t=resource/res_list&verify=1)，
 这有助于你使用```Fluwx```。

### 目前功能
* 文本分享。
* 网站分享。
* 图片分享。
* 音乐分享。
* 视频分享。
* 小程序分享。
* 发送Auth认证。

## 引入
在```pubspec.yaml```文件中添加如下代码：
```yaml
dependencies:
  fluwx: ^0.0.3
```

## 初始化
使用```Fluwx```前，需要进行初始化操作：
 ```dart
 Fluwx.registerApp(RegisterModel(appId: "your app id", doOnAndroid: true, doOnIOS: true));
 ```
 - ```appId```：在微信平台申请的appId。
 - ```doOnAndroid```:是否在android平台上执行此操作。
 - ```doOnIOS```:是否在平台上执行此操作。</br>
 每一个字段都是非必须的，但是如果不传```appId```或```doOnAndroid: false```或者```doOnIOS: false```，在使用前请务必手动注册```WXApi```，以保证
 ```Fluwx```正常工作。
 注册完成后，请在使用```Fluwx```前在对应平台添加如下代码：
 Android上：
 ```Kotlin
 FluwxShareHandler.setWXApi(wxapi)
 ```
 iOS上：
 ```objective-c
isWeChatRegistered = YES;
 ```

> 注意：尽管可以通过Fluwx完成微信注册，但一些操作依然需要在对应平台进行设置，如配置iOS的URLSchema，Android上的WXEntryActivity等。

### 传送门
* [分享功能](docs/SHARE.md)。
* [发送Auth认证](docs/SEND_AUTH.md)。

### 更多功能敬请请期待

