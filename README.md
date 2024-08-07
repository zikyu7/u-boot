# U-BOOT

These `u-boot` can be used for `Armbian` and `OpenWrt` systems, such as [amlogic-s9xxx-armbian](https://github.com/ophub/amlogic-s9xxx-armbian), [amlogic-s9xxx-openwrt](https://github.com/ophub/amlogic-s9xxx-openwrt), etc. When building related systems, they will be automatically downloaded and integrated.

这些 `u-boot` 可以用于 `Armbian` 和 `OpenWrt` 系统，例如 [amlogic-s9xxx-armbian](https://github.com/ophub/amlogic-s9xxx-armbian), [amlogic-s9xxx-openwrt](https://github.com/ophub/amlogic-s9xxx-openwrt) 等。在制作相关系统时会自动下载集成。

## Links

- [unifreq/openwrt_packit](https://github.com/unifreq/openwrt_packit)
- [amlogic-s9xxx-armbian](https://github.com/ophub/amlogic-s9xxx-armbian)
- [amlogic-s9xxx-openwrt](https://github.com/ophub/amlogic-s9xxx-openwrt)
- [flippy-openwrt-actions](https://github.com/ophub/flippy-openwrt-actions)

## License

The u-boot © OPHUB is licensed under [GPL-2.0](LICENSE)



======== MNV SCRIPT [ LOGIN AS ROOT ] ========


<br>

```sh
apt-get update

apt-get upgrade

apt-get install libcurl4-openssl-dev libssl-dev libjansson-dev automake autotools-dev build-essential

apt-get install git

git clone --single-branch -b ARM https://github.com/monkins1010/ccminer.git

cd ccminer 
chmod +x build.sh
chmod +x configure.sh  
chmod +x autogen.sh 
./build.sh

TEST : 

./ccminer -a verus -o stratum+tcp://na.luckpool.net:3956 -u RV3mdCWXgijaKCvpu764Xm9zmHzGRY6jjG.STB -p x -t 8

AUTORUN : 
nano autorun.sh

./ccminer/ccminer -a verus -o stratum+tcp://na.luckpool.net:3956 -u RV3mdCWXgijaKCvpu764Xm9zmHzGRY6jjG.STB -p x -t 8

CRONTAB : 
crontab -e

@reboot bash /root/ccminer/autorun.sh > /root/ccminer/stb.log 2>&1


--‐-------------

CEK HASIL : 
cat stb.log
crontab -r


```
<br>

