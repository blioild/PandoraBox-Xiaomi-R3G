# 自修改 Xiaomi-R3G 的 PandoraBox 固件。
### 源固件地址：[点我下载](http://downloads.pangubox.com:6380/pandorabox/19.02/targets/ralink/mt7621/PandoraBox-ralink-mt7621-xiaomi-r3g-2019-02-01-git-0231ad4b5-squashfs-sysupgrade.bin) ###
### 此固件地址：[点我下载](https://raw.githubusercontent.com/blioild/PandoraBox-Xiaomi-R3G/main/PandoraBox-ralink-mt7621-xiaomi-r3g-2019-02-01-git-0231ad4b5-squashfs-sysupgrade.bin) ###

### 此固件使用 PandoraBox 官网上的 Imagebuilder 和 SDK 生成编辑生成。除了第三方插件外，其他地方与源固件并没有太大区别。 ###

# 此固件的一些说明：

- 1、删除了源固件的 Smartinfo （权限不足导致无法运行）。
- 2、添加了：
>- [coremark](https://github.com/coolsnowwolf/packages/tree/master/utils/coremark)
>- [ddns-scripts_aliyun](https://github.com/coolsnowwolf/lede/tree/master/package/lean/ddns-scripts_aliyun)
>- [ddns-scripts_dnspod](https://github.com/coolsnowwolf/lede/tree/master/package/lean/ddns-scripts_dnspod)
>- [smartdns](https://github.com/pymumu/openwrt-smartdns)
>- [ssr-plus](https://github.com/maxlicheng/luci-app-ssr-plus)
>- vim , nano , iperf3 , htop , lrzsz , webui-aria2 , ttyd , zerotier , minidlna , material 主题
- 3、修复了 miniupnp 无法正常映射的问题（将自带的 miniupnp 替换为 lean 源的 [miniupnp](https://github.com/coolsnowwolf/packages/tree/master/net/miniupnpd)）。初次使用 zerotier 可能导致路由器网络掉线，无法进入后台，可以直接断电重启，也可以使用 zerotier 登入后台重启，一般来说这种情况只会出现一次。如果 ttyd 无法使用，建议重启路由器或更换浏览器。ssr-plus 比较老旧，只支持ss/ssr/v2ray，使用 SDK 无法成功编译最新的 ssr-plus 及其组件。
- 4、建议使用 pb-boot 刷入，或者在 PandoraBox 固件里不保留配置刷入，以免出现一些奇奇怪怪的问题。
### 目前固件里集成的插件全部都能正常运行，开始养老，或许以后发现 BUG 的话会更新。 ###