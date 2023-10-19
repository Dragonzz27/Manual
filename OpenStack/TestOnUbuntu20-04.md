#### Deploy Physically Openstack On Ubuntu20.04

1. 主机准备

|  主机环境  |  IP地址   |
| :--------: | :-------: |
| controller | 10.0.0.11 |
|  computer  | 10.0.0.31 |

2. 节点配置
    1. 控制节点
    ```shell
    vim /etc/sysconfig/network-scripts/ifcfg-eth0
    ```
    ```shell
    TYPE=Ethernet
    BOOTPROTO=static
    NAME=eth0
    DEVICE=eth0
    ONBOOT=yes
    IPADDR=10.0.0.11    #修改为指定IP地址
    NETMASK=255.255.255.0
    GATEWAY=10.0.0.2
    DNS1=223.5.5.5
    ```
    ```shell
    systemctl restart network   #修改完成后重启网卡
    ```
    2. 计算节点
    ```shell
    vim /etc/sysconfig/network-scripts/ifcfg-eth0
    ```
    ```shell
    TYPE=Ethernet
    BOOTPROTO=static
    NAME=eth0
    DEVICE=eth0
    ONBOOT=yes
    IPADDR=10.0.0.31    #修改为指定IP地址
    NETMASK=255.255.255.0
    GATEWAY=10.0.0.2
    DNS1=223.5.5.5
    ```
    ```shell
    systemctl restart network 	#修改完成后重启网卡
    ```