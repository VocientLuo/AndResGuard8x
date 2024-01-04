#  forked from https://github.com/shwenzhang/AndResGuard

# Android资源混淆工具使用说明 #


## Changes

- 支持8.x以上AGP


## 构建步骤

* 1、直接运行publish
* 2、默认会把aar生成在当前项目下```repo```文件夹下
* 3、使用中可以添加本地maven依赖指向该repo

![img](./screenshot/ss1.png)


没做公仓推送

## 有需要可自行推送到远程仓

* 1、 修改根目录下的```build.gradle```文件相关配置：

```groovy
ext {
    javaVersion = JavaVersion.VERSION_17

    POM_PACKAGING = "pom"
    POM_DESCRIPTION = "Android Resource Proguard Core Lib"

    versionName = "1.1.4.11"
    // 默认 false, true 代表推远程maven仓
    publishToServer = false
    groupID = "com.xluo.plugin"
    // aar local path
    localPath = './repo'
}
```

* 2、配置```gradle.properties```中的maven信息

```groovy

# maven info
REPOSITORY_URL=***
GROUP_LIB=com.xzluo.lib
NEXUS_USERNAME=***
NEXUS_PASSWORD=***
```

* 3、执行publish即可推送到远程仓

亲测在debug模式下能正常工作，未做详细测试。


   
