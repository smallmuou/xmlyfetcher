# xmlyfetcher 【全新升级!!!】

> 该工具用于下载喜马拉雅歌曲资源，可以下载单个音频资源，也可以下载整个专辑. 喜欢的请打个红心!!!

[![asciicast](https://asciinema.org/a/4jz6NqQIeLZL7weqpZDQ17Wi6.png)](https://asciinema.org/a/4jz6NqQIeLZL7weqpZDQ17Wi6?autoplay=1)

## 安装
1. 确认是否安装Python，一般系统会自带

```
python -V
```

2. 安装该工具

```bash
wget https://raw.githubusercontent.com/smallmuou/xmlyfetcher/master/xmlyfetcher
sudo cp xmlyfetcher /usr/local/bin
sudo chmod +x /usr/local/bin/xmlyfetcher
```

## 使用

```bash
xmlyfetcher 专辑ID 类型 参数

专辑ID可以通过浏览器URL获取，如https://www.ximalaya.com/album/2677356，则专辑ID为2677356

类型分为3种，分别是all、page、track

all - 下载整个专辑
page - 下载若干页号，支持传递多个页号，从1开始，每页30
track - 下载若干歌曲，支持传递多个曲目ID，曲目ID可以通过浏览器URL获取，比如点击某个曲目，其URL为https://www.ximalaya.com/sound/25202，则曲目ID为25202

# 下载专辑
xmlyfetcher 12891461 all

# 下载专辑前2页
xmlyfetcher 12891461 page 1 2

# 下载单个曲目
xmlyfetcher 12891461 track 211393643

```
PS: 可以使用`xmlyfetcher -h`查看更详细的帮助

```
xmlyfetcher version 2.0.0 by smallmuou

USAGE: xmlyfetcher [OPTIONS] albumId type [type-param1 [type-param1 ...]]

DESCRIPTION:
    This tool is used to download tracks under ximalaya.com.

    albumId - the id of album, you can see from url,like https://www.ximalaya.com/album/2677356, the albumId is 2677356
    type - all/page/track, when type is all, no type-params required; when type is page, the type-params is the pagenum (start with 1); when type is track, the type-params is trackid;
    trackId - the id of track, you can see from url,like https://www.ximalaya.com/sound/25202, the trackId is 25202

OPTIONS:
    -h      Show this help message and exit.

EXAMPLES:
    xmlyfetcher 12891461 all
    xmlyfetcher 12891461 page 1 2 3
    xmlyfetcher 12891461 track 211393643
```

## 版本记录
* 2.0.0（2023.1.31）
    - 修正无法下载BUG
    - 支持指定若干页面下载
    - 参数调整

* 1.1.0（2019.9.12）
    - 改为接口获取专辑信息，而不是解析HTML

* 1.0.3（2019.9.10）
    - 移除了jshon依赖
    - 修复无法获取专辑问题

* 1.0.2
    - 修复无法获取专辑问题

* 1.0.1
    - 支持下载一个专辑的所有歌曲（支持翻页）

* 1.0.0
    - 支持下载单个歌曲和专辑

* 1.1.1（2019.9.29）
    - 修复下载资源名称包括非法字母，导致"没有那个文件或目录"问题

## 许可

该开源工具具有MIT许可协议. 本工具仅限个人学习，不用于商业等用途. 所涉及的音视频资源版权归喜马拉雅所有.
