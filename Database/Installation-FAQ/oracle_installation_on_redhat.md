Oracle 数据库安装过程FAQ
------------------------
March 2015

# Software Version
- **System Version:**
Red Hat Enterprise Linux Sever release 6.4 (Santiago)
Linux 下查看系统版本命令

    `# cat /etc/issue`

- **Database Version:**
Release 11.2.0.1.0 Production
Linux下查看数据库版本命令

    `# ./sqlplus -v`

**Note:**版本11.2.0.1.0会出现较多package缺失的情况，选择高版本的数据库安装包可以解决这个问题。

# Software Requirements
- check all the packages listed on Oracle Official Documentation

# Configure yum Source

    [root@node~] # cat /etc/yum.repos.d/rhel
    rhel5.repo rhel-debuginfo.repo
    [root@node~] # cat /etc/yum.repos.d/rhel5.repo

    [Server]
    name=server
    baseurl=file:///mnt/Server/
    enabled=1
    gpgcheck=0

    [ClusterStorage]
    name=server
    baseurl=file:///mnt/ClusterStorage/
    enabled=1
    gpgcheck=0
