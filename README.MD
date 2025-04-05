# 项目介绍

在 mac m系列下，实现与服务器进行便捷的文件上传和下载操作。


# 步骤

1.安装支持 rz 和 sz 命令的 lrzsz：`brew install lrzsz`

> 等了挺长时间的。

2.在本地 ~/bin 目录下保存 iterm2-send-zmodem.sh 和iterm2-recv-zmodem.sh 两个脚本

3.设置一下两个脚本的权限，一般 chmod +x 就行了

```bash
chmod  +x  ~/bin/iterm2-send-zmodem.sh  ~/bin/iterm2-recv-zmodem.sh
```

4.设置 iTerm2 的 Tirgger 特性，Settings->Profiles->Advanced中的Tirgger

添加两条 trigger，分别设置 Regular expression，Action，Parameters，Instant 如下：

```
1.第一条
        Regular expression: \*\*B0100
        Action: Run Silent Coprocess
        Parameters: ~/bin/iterm2-send-zmodem.sh
        Instant: checked
2.第二条
        Regular expression: \*\*B0000000000000
        Action: Run Silent Coprocess
        Parameters: ~/bin/iterm2-recv-zmodem.sh
        Instant: checked
```
