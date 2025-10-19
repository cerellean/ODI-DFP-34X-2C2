# ODI-DFP-34X-2C2
ODI DFP-34X-2C2固件
# 刷入固件
登陆猫棒后台，默认地址 192.168.1.1，默认用户名和密码都是 admin（需要确保电脑在同一个网段才能访问到）

登陆后进入固件升级，选择刚才下载的 tar 文件，点击升级

重启之后 telnet登录，擦除重置
```
# flash_eraseall /dev/mtd3
# reboot
```
# 配置LOID或者PASSWARD
升级完成后再次登陆猫棒后台，填入LOID或者PLOAM密码（选ASCII格式)


# 配置 MAC 和 MACKEY
升级完成后再次登陆猫棒后台

MAC：光猫的 MAC 地址

MACKEY：hsgq1.9a+大写的光猫 MAC 地址的小写 md5 值，如 MAC 地址是 XXXXXXXXXXXX, 则获取hsgq1.9aXXXXXXXXXXXX的 md5 值即可，可以使用命令行或者在线网站进行计算(https://www.ip33.com/md5.html ）， 填入32位MD5码

OUI：配置值为 111111，这个配置在任何文档中均未提到，但是实际影响到了拨号，未配置之前拨号一直没有响应，配置后可以成功拨号（或许和其他配置有关）

其他配置：非必须，参考图片内容进行配置即可（如果拨号失败建议修改为一样的）
