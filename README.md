# kms.sh

wget --no-check-certificate https://raw.githubusercontent.com/becapital/kms.sh/master/kms.sh && chmod +x kms.sh && ./kms.sh


安装完成后，输入以下命令查看端口号 1688 的监听情况


netstat -nxtlp | grep 1688

返回值类似于如下这样就表示 OK 了：

tcp        0      0 0.0.0.0:1688                0.0.0.0:*                   LISTEN      3200/vlmcsd     

tcp        0      0 :::1688                     :::*                        LISTEN      3200/vlmcsd 

本脚本安装完成后，会将 KMS 服务加入开机自启动。

使用命令：

启动：/etc/init.d/kms start

停止：/etc/init.d/kms stop

重启：/etc/init.d/kms restart

状态：/etc/init.d/kms status

卸载方法：

使用 root 用户登录，运行以下命令：

./kms.sh uninstall
