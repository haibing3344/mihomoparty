---
title: Mihomo Party 使用教程，配置指南
description: Mihomo Party 是一款基于Mihomo的客户端，支持Windows、macOS、Linux等系统。下面介绍 Mihomo Party 的安装和使用方法，帮助你快速上手使用 Mihomo Party。
---

::: tip 提示
Mihomo Party 已更名为[Clash Party](https://clashparty.men)，后续所有更新和维护都将在Clash Party项目进行。
:::

# Mihomo Party 使用教程，配置指南

下面介绍 Mihomo Party 的安装和使用方法，帮助你快速上手使用 Mihomo Party。

## Mihomo Party 安装/启动

从首页[Mihomo Party下载](/download.md)中找到对应系统的版本进行下载安装，本文将以MacOS版为例详细介绍如何使用 Mihomo Party。

- 对于Windows版，安装完成后，需要右击选择管理员运行，否则会出现如下图的错误：


- 对于macOS版，第一次打开可能会提示“开发者无法验证”或“应用已损坏”，可以在终端应用中执行以下命令解决：
```bash
sudo xattr -r -d com.apple.quarantine /Applications/mihomo-party.app
```

## Mihomo Party 订阅导入
在机场购买订阅后，会得到一个订阅链接，这里以TNT Cloud为例，复制订阅地址，如下图所示：
![TNT Cloud 订阅链接](/assets/tntcloud.png)

在右侧的订阅链接输入框中粘贴订阅链接(如果你还没有购买机场订阅，可以参考[机场推荐](/docs/recommendations.md))，点击导入，即可完成订阅导入。
![Mihomo Party 订阅导入](/assets/mihomo-party-subscribe.png)

导入成功后如图所示：
![Mihomo Party 订阅导入成功](/assets/mihomo-party-subscribe-success.png)


## Mihomo Party 节点选择/代理切换

订阅导入后，可在代理组中看到订阅中包含的所有代理节点，你可以根据自己的需求选择节点，也可以点击右上方测速按钮，然后选择最快的节点使用。
![Mihomo Party 代理组](/assets/mihomo-party-group.png)
![Mihomo Party 节点选择](/assets/mihomo-party-node.png)

## Mihomo Party 开启代理
在导入订阅以及选择好节点以后，就可以启动Mihomo Party开始使用了。只需要在侧边栏左上角打开系统代理，就可以成功进行科学上网了。通常情况下，不需要开启虚拟网卡(TUN模式)就可以正常翻墙，但如果失败，则推荐开启虚拟网卡进行尝试。
![Mihomo Party 开启代理](/assets/mihomo-party-enable.png)

至此，Mihomo Party 已经成功配置完毕，最小化托盘。你可以打开浏览器，试着访问YouTube或者Google测试是否可以访问。
::: tip ⚠️注意
- 如果无法科学上网，可以尝试重启电脑或者重启Mihomo Party。
- 当不需要科学上网的时候，记得关闭系统代理。
:::

::: tip 🎉 节点推荐
- 🚀 [Cyberguard: 解锁Netflix/Hbo/Disney+/Dazn等流媒体,18.00元/月](https://c.jichangs.com/cyberguard)
- 🚀 [优信云：IEPL/IPLC 高速专线，￥15.00/月](https://c.jichangs.com/youxinyun)<br>
- 🚀 [尔湾云：最大峰值1000Mbps，全流媒体及ChatGPT解锁！最低12元/月](https://c.jichangs.com/erwan)<br>
- 🚀 [TNTCloud：新开机场，季付30，每月低至￥10.00/月](https://c.jichangs.com/tnt)<br>
- 🚀 [魔戒：不限时，不限制使用人数，直至套餐流量用完，低至￥14.9/130G流量。](https://c.jichangs.com/mojie)<br>
- 🚀 [宝可梦星云：新用户首单：9折优惠码：9999，低至5.9/月 ](https://c.jichangs.com/pokemon)
- 🚀 [NanoCloud: 绑定TG机器人每天领取免费流量，月付最低1元/月](https://c.jichangs.com/nanocloud)
:::