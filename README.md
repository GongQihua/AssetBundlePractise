# AssetBundle实战（AB打包）

## 简介

AssetBundle打包实战项目，主要是AssetBundle怎么打包的，怎么加载以及卸载的过场和原理，随便倒了个资源包进来，进行实操。

项目使用XML文件进行打包文件配置，采用字典数据结构加引用计数进行AB包的自动加载与卸载。

热更新方案如下:本地和服务器都存有相应的资源包版本信息文件，本地向服务器发送资源更新请求，对照本地MD5码和服务器中MD5码，不同则从服务器重新下载相应的AB包到本地程序，最后加载AB包资源。

> 打出的ab资源在工程同级的AssetBundle下
>
> 可以无缝切换编辑器和AB加载方式
>
> 注意AB模式下，改完资源记得Tools/ResBuild一下
>
> 支持同步异步等方式
>
> 具体的打包配置在BuildSetting.xml里配置即可，具体精细到文件还是文件夹都可以。

主要工程代码在AssetBundleFramework下，core和editor

## 链接

详细文档：https://gongqihua.github.io/

演示Demo在demo文件夹下：传送门