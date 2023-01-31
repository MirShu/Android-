# Android空包签名

很多应用平台多个帐号出现混淆发布应用的时候就需要 所谓的 “应用认领”，那应用认领就需要牵涉到空包签名，打包再上传到平台，这个时候就需要了解平台给你一个它们自己的空包让你签完名后上传的一个具体流程，
那如何空包签名：

# 第一、从平台上下载一个它们提供的一个空包。

# 第二，签名 cmd打开控制台

```
 jarsigner -verbose -keystore F:\51bjtong.keystore -signedjar F:\YXT\xiaomi\verification-signed.apk F:\YXT\xiaomi\verification.apk 51bjtong
```

我的签名文件是放在F盘地下的，找到绝对路径

F:\51bjtong.keystore 是自己的app签名文件路径

F:\YXT\xiaomi\verification-signed.apk 是签完名后apk的命名文件路径

F:\YXT\xiaomi\verification.apk 是平台下载下来的空包apk文件路径

51bjtong 这个是你自己apk别名 （keyAlias）值

# 第三、这些路径都没错就开始输入打包签名密码
![QQ截图20230110170205](https://user-images.githubusercontent.com/13359093/211512248-6d04304f-3075-45e0-8280-db3af7cd991c.png)

输入进去就可以了（记住，这地方输入的时候是不显示密码的，所以要注意大小写，和别输入错了）

# 最后一步，如果密码都输入正确无误，

![QQ截图20230110170600](https://user-images.githubusercontent.com/13359093/211512474-4e25308f-d784-4a93-ad30-19e0534d82da.png)

就会发现F:\YXT\xiaomi\verification-signed.apk这个路径下的这个apk文件了，这就是空包签好名的，直接上传上去就可以了
