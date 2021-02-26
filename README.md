# 在CentOS 7 & 8 （编译按照4.19 & 5.10版本Linux内核）

## 下载内核源码
http://www.kernel.org/

## 参考材料
1. 鸟哥私房菜. http://linux.vbird.org/linux_basic/0540kernel.php

## 问题（2、3最好提前做，否则编译很久后报错重来费时间）
1. 在make bzImage时缺什么工具装什么工具
2. No rule to make target 'certs/rhel.pem', needed by 'certs/x509_certificate_list'  ==》 修改linux内核文件的.config文件，查找CONFIG_SYSTEM_TRUSTED_KEYS，然后置空
3. error:BTF:.tmp_vmlinux.btf:pahole(pahole) is not available  ==> yum install epel-release yum install dwarves


## 相关
若/usr/src/kernels下无内核源码  == 》yum install kernel-devel -y
