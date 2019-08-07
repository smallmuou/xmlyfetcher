# xmlyfetcher

> 该工具用于下载喜马拉雅歌曲资源，可以下载单个音频资源，也可以下载整个专辑. 喜欢的请打个红心!!!

[![asciicast](https://asciinema.org/a/4jz6NqQIeLZL7weqpZDQ17Wi6.png)](https://asciinema.org/a/4jz6NqQIeLZL7weqpZDQ17Wi6?autoplay=1)

## 安装

1. 安装jshon

```bash
wget http://kmkeen.com/jshon/jshon.tar.gz
tar xzvf json.tar.gz
cd jshon-20120914
make
sudo cp jshon /usr/local/bin/
```
PS: jshon下载地址可能会变更，请根据官网提示下载.

2. 安装该工具

```bash
git clone https://github.com/smallmuou/xmlyfetcher.git
cd xmlyfetcher
sudo cp xmlyfetcher /usr/local/bin/
sudo chmod +x /usr/local/bin/xmlyfetcher
```

## 使用

```bash
# 下载专辑
xmlyfetcher https://www.ximalaya.com/ertong/260744/

# 下载单个歌曲
xmlyfetcher 76515823

# 下载到指定目录
xmlyfetcher -o ~/Downloads https://www.ximalaya.com/ertong/260744/
```
PS: 可以使用`xmlyfetcher -h`查看更详细的帮助，注意以上地址是当前有效地址，可能会失效，请从喜马拉雅官网获取最新地址

## 版本记录
* 1.0.0

支持下载单个歌曲和专辑

* 1.0.1

支持下载一个专辑的所有歌曲（支持翻页）

* 1.0.2

修复无法获取专辑问题

## 许可

该开源工具具有MIT许可协议. 本工具仅限个人学习，不用于商业等用途. 所涉及的音视频资源版权归喜马拉雅所有.