# Android 6.0（API 23）以上org.apache.http.*的使用

Android 6.0（API 23）以上不再提供org.apache.http.*，只保留几个类。GOOGLE建议使用HttpUrlConnection类，因为它可以通过透明压缩和响应缓存减少网络使用，并可最大限度降低耗电量。如需继续使用Apache HTTP API,必须在build.gradle文件中声明以下编译时依赖项：
```
android {
    useLibrary 'org.apache.http.legacy'
}
```
完整截图：

![image](http://img.blog.csdn.net/20150928143049042)

参考文档

1. [http://blog.csdn.net/yy1300326388/article/details/48784475](http://blog.csdn.net/yy1300326388/article/details/48784475)
2. [https://developer.android.com/intl/zh-cn/preview/behavior-changes.html#behavior-apache-http-client](https://developer.android.com/intl/zh-cn/preview/behavior-changes.html#behavior-apache-http-client)
