#### AutoBuild-OpenWrt

#### 源码来源：
[![esir](https://img.shields.io/badge/AutoBuild-esir-red.svg?style=flat&logo=appveyor)](https://github.com/esirplayground/AutoBuild-OpenWrt)
 [![Lienol](https://img.shields.io/badge/passwall-openwrt-blueviolet.svg?style=flat&logo=appveyor)](https://github.com/xiaorouji/openwrt-passwall) 
[![immortalwrt](https://img.shields.io/badge/immortalwrt-openwrt-orange.svg?style=flat&logo=appveyor)](https://github.com/immortalwrt/immortalwrt) 
[![Lean](https://img.shields.io/badge/package-Lean-blueviolet.svg?style=flat&logo=appveyor)](https://github.com/coolsnowwolf/lede) 
[![P3TERX](https://img.shields.io/badge/Actions-P3TERX-success.svg?style=flat&logo=appveyor)](https://github.com/P3TERX/Actions-OpenWrt)

##### 固件发布:

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/kenzok8/openwrt_Build?style=for-the-badge&label=固件下载)](https://github.com/kenzok8/openwrt_Build/releases/latest)


##### 固件下载链接

- [Lienol_22.03固件地址](https://op.dllkids.xyz/op/firmware/Lienol/)
- [Lean固件地址](https://op.dllkids.xyz/op/firmware/Lean/)
- [immortalwrt-21.02固件](https://op.dllkids.xyz/op/firmware/ctc_21.02/)
- [immortalwrt-18.06固件](https://op.dllkids.xyz/op/firmware/ctc_18.06/)
- [nanopi-r2s固件下载](https://op.dllkids.xyz/op/firmware/nanopi-r2s/)
- [nanopi-r4s固件下载](https://op.dllkids.xyz/op/firmware/nanopi-r4s/)

### 默认插件包含:

+ SSR Plus 
+ passwall2
+ bypass
+ openclash
+ 动态DDNS
+ UPNP 自动端口转发
+ 默认多个主题
+ 默认管理 IP: 192.168.1.252, 用户名 root，密码 password

* 修改默认ip

```bash
sed -i 's/192.168.1.1/192.168.3.1/g' package/base-files/files/bin/config_generate
```
* 删除原主题	
```bash
rm -rf package/lean/luci-theme-argon
```

* 添加新的主题
```bash
git clone https://github.com/kenzok8/luci-theme-ifit.git package/lean/luci-theme-ifit
```
* 添加常用软件包
```bash
git clone https://github.com/kenzok8/openwrt-packages.git package/openwrt-packages
```
* 删除默认密码
```bash
sed -i "/CYXluq4wUazHjmCDBCqXF/d" package/lean/default-settings/files/zzz-default-settings
```

* 取消bootstrap为默认主题	
```bash
sed -i '/set luci.main.mediaurlbase=\/luci-static\/bootstrap/d' feeds/luci/themes/luci-theme-bootstrap/root/etc/uci-defaults/30_luci-theme-bootstrap
```


