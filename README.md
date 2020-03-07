# jumpserver_onekey_install
基于官方jms_install.sh脚本修改
1. 修正Django依赖版本错误
2. 修正数据库配置格式问题

# 安装
前提条件：
1. 服务器为centos7系统
2. 服务器可以联网
3. 服务器基本配置需求请参考官网

安装步骤：
1. cd /opt
2. git clone https://github.com/wei588765/jumpserver_onekey_install.git
3. mv /opt/jumpserver_onekey_install/jms_install.sh /opt
4. sh /opt/jms_install

# 常见错误
问题1：邮箱无法使用

答：如果使用云服务器，需要申请开通25端口，或者使用465端口


问题2：能收到测试邮件，但是新建用户收不到邮件

答：重启redis服务后，重启jumpserver


问题3：终端无法连接跳板机

答：终端连接跳板机默认使用ssh端口，密钥在新建用户时可以自动生成，也可以自行生成密钥然后设置公钥
