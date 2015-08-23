# Lesson-01 课程简介及环境设置

# 安装

```
vagrant up
vagrant ssh

$ sudo yum update

exit
vagrant reload
vagrant ssh

# rebuild VirtualBox Guest Additions
sudo yum -y install kernel-devel-3.10.0-229.7.2.el7.x86_64
sudo yum install -y gcc

sudo /etc/init.d/vboxadd setup

```

安装Docker（docker-engine）

```
$ sudo curl -sSL https://get.docker.com/ | sh
+ sudo -E sh -c 'sleep 3; yum -y -q install docker-engine'
warning: /var/cache/yum/x86_64/7/docker-main-repo/packages/docker-engine-1.7.1-1.el7.centos.x86_64.rpm: Header V4 RSA/SHA1 Signature, key ID 2c52609d: NOKEY
Public key for docker-engine-1.7.1-1.el7.centos.x86_64.rpm is not installed
Importing GPG key 0x2C52609D:
 Userid     : "Docker Release Tool (releasedocker) <docker@docker.com>"
 Fingerprint: 5811 8e89 f3a9 1289 7c07 0adb f762 2157 2c52 609d
 From       : https://yum.dockerproject.org/gpg

If you would like to use Docker as a non-root user, you should now consider
adding your user to the "docker" group with something like:

  sudo usermod -aG docker vagrant

Remember that you will have to log out and back in for this to take effect!

```

启动
```
sudo service docker start
```

自启动
```
sudo service enable start
```


```
sudo vi /lib/systemd/system/docker.service
/usr/bin/docker --registry-mirror=http://liubin.m.alauda.cn -d -H fd://
sudo systemctl daemon-reload
```

# 参考资料

- 灵雀云镜像加速设置方法

http://docs.alauda.cn/?page_id=137

- March 21, 2013 Solomon gives Docker lightning talk a PyCon US

https://www.youtube.com/watch?t=27&v=9xciauwbsuo

- Operating-system-level virtualization implementations

https://en.wikipedia.org/wiki/Operating_system-level_virtualization#Implementations

- hashicorp公司主页

https://hashicorp.com/

- Docker toolbox

https://www.docker.com/toolbox



