##### tftp

```
sudo apt-get install tftp-hpa tftpd-hpa
sudo apt-get insatll xinetd
mkdir /home/xf/tftpboot
chomd 777 /home/xf/tftpboot
sudo vim /etc/xinetd.d/tftp
sudo service tftpd-hpa start
sudo vim /etc/default/tftpd-hpa
SUDO service tftpd-hpa restart
```

/etc/xinetd.d/tftp下内容

```
service tftp
{
        socket_type     = dgram
        protocol        = udp
        wait            = yes
        user            = root
        server          = /usr/sbin/in.tftpd
        server_args     = -s /home/xf/tftpboot/
        disable         = no
        per_source      = 11
        cps             = 100 2
        flags           = IPv4
}
```

/etc/default/tftpd-hpa下内容

```
# /etc/default/tftpd-hpa

TFTP_USERNAME="tftp"
TFTP_DIRECTORY="/home/xf/tftpboot/"
TFTP_ADDRESS=":69"
TFTP_OPTION="-l -c -s"
```

本地测试

```
tftp 127.0.0.1
get /home/xf/tftpboot/test.txt	这里需要绝对路径 很奇怪
```

客户端测试

```
tftp -g -l /etc/config.ini -r /home/xf/tftpboot/config.ini 192.168.9.2
```