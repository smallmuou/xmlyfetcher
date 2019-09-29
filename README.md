# xmlyfetcher

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
xmlyfetcher 网页路径，可以直接从浏览器中复制

# 下载专辑
xmlyfetcher https://www.ximalaya.com/ertong/12891461/

# 下载专辑单页(带pxx)
xmlyfetcher https://www.ximalaya.com/ertong/12891461/p2/

# 下载单个曲目
xmlyfetcher https://www.ximalaya.com/ertong/12891461/211393643

# 下载到指定目录
xmlyfetcher -o ~/Downloads https://www.ximalaya.com/ertong/12891461/211393643
```
PS: 可以使用`xmlyfetcher -h`查看更详细的帮助，注意以上地址是当前有效地址，可能会失效，请从喜马拉雅官网获取最新地址

## 版本记录
* 1.0.0

    - 支持下载单个歌曲和专辑

* 1.0.1

    - 支持下载一个专辑的所有歌曲（支持翻页）

* 1.0.2

    - 修复无法获取专辑问题

* 1.0.3（2019.9.10）

    - 移除了jshon依赖
    - 修复无法获取专辑问题

* 1.1.0（2019.9.12）
    - 改为接口获取专辑信息，而不是解析HTML

* 1.1.1（2019.9.29）
    - 修复下载资源名称包括非法字母，导致"没有那个文件或目录"问题

## 许可

该开源工具具有MIT许可协议. 本工具仅限个人学习，不用于商业等用途. 所涉及的音视频资源版权归喜马拉雅所有.