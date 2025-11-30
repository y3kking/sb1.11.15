本脚本用于在 Linux 服务器上快速安装、配置和管理 [Sing-Box](https://github.com/SagerNet/sing-box)，特别针对 Hysteria2 和 VLESS Reality 协议优化。

<details>
  <summary>.</summary>

## VPS仅IPV6/IPV4 脚本推荐

- [WARP 一键脚本](https://gitlab.com/fscarmen/warp)先套IPV4/IPV6：

```bash
wget -N https://gitlab.com/fscarmen/warp/-/raw/main/menu.sh && bash menu.sh [option] [lisence/url/token]
```
---

## vps实用工具箱推荐

- [老王一键工具箱](https://github.com/eooce/ssh_tool)：此工具，适合小白用户轻松搭建上网节点，跟我的脚本一样简单好用，轻松上手！

```bash
curl -fsSL https://raw.githubusercontent.com/eooce/ssh_tool/main/ssh_tool.sh -o ssh_tool.sh && chmod +x ssh_tool.sh && ./ssh_tool.sh#建议快捷命令改为 w 避免冲突！
```

- [科技lion一键脚本](https://kejilion.sh/index-zh-CN.html)：适合无基础小白网站的建设与维护。

```bash
bash <(curl -sL kejilion.sh)#建议快捷命令改为 i
```
---

## ssh终端连接/实用网站
  
- 下载并安装SSH连接工具:
  - [Finalshell电脑版:](https://www.hostbuf.com/t/988.html)稳定好用！基本人手一个。
  - [WindTerm](https://github.com/kingToolbox/WindTerm/releases/tag/2.7.0)开源免费

- 安卓/iOS/PC 推荐客户端：
  - [Karing](https://github.com/KaringX/karing/releases)（全平台免费开源，强烈推荐）
  - [nekobox](https://github.com/MatsuriDayo/NekoBoxForAndroid/releases)
  - [husi](https://github.com/xchacha20-poly1305/husi/releases)
  - [Clash-Meta](https://github.com/MetaCubeX/ClashMetaForAndroid/releases)
  - [hiddify](https://github.com/hiddify/hiddify-next/releases)
  - [v2rayNG](https://github.com/2dust/v2rayNG/releases)(安卓设备首选)
  - [Clash-Verge](https://github.com/clash-verge-rev/clash-verge-rev/releases)
  - [v2rayN](https://github.com/2dust/v2rayN/releases)(Win电脑PC端)

- 实用网站推荐：
    - [libretv-自建影视](https://053312d1.libretv-edb.pages.dev/)进入密码:123
    - [磁力熊](https://www.cilixiong.org/)也是影视！
    - [IP质量检测](https://ipjiance.com/)
    - [IP纯净度检测](https://scamalytics.com/​)
    - [节点测速](https://fiber.google.com/speedtest/)
    - [CF网址：](https://www.cloudflare.com/zh-cn/)CloudFlare
    - [ip泄露真实地址检测1](https://dw.jhb.ovh/)，非你所处真实地址则没泄露！
    - [ip泄露真实地址检测2](https://ipleak.net/)



</details>

---

## ✨ 使用方法


**更新系统(可选)：**

```bash
apt-get update && apt-get install -y curl
```
**套warp(IPV4可选)：**

```bash
wget -N https://gitlab.com/fscarmen/warp/-/raw/main/menu.sh && bash menu.sh [option] [lisence/url/token]
```

**命令1. 拉取脚本并启动：(报错则更新系统或下载curl组件)(安装命令不要去做一个保存后面会优化启动命令)**

```bash
curl -fsSL "https://github.com/y3kking/sb1.11.15/raw/main/lvhy.sh" -o lvhy.sh &&
curl -fsSL "https://github.com/y3kking/sb1.11.15/raw/main/modify_node_params.sh" -o modify_node_params.sh &&
curl -fsSL "https://github.com/y3kking/sb1.11.15/raw/main/bbr_manage.sh" -o bbr_manage.sh &&
curl -fsSL "https://github.com/y3kking/sb1.11.15/raw/main/install.sh" -o install.sh &&
chmod +x lvhy.sh modify_node_params.sh bbr_manage.sh install.sh &&
bash ./lvhy.sh
```

**命令2. 再次运行可启动脚本，之后可快捷命令： `box`**

```bash
sudo bash lvhy.sh
```

脚本将以 root 权限运行，并显示主菜单。

## 注意事项

- **防火墙**：只需放行相关端口。
  - 例如 Re 用 443，H2 用 8443：
    ```bash
    sudo ufw allow 443/tcp
    sudo ufw allow 8443/tcp
    sudo ufw allow 8443/udp # Hysteria2 需要 UDP
    sudo ufw reload
    ```
- **端口选择：选 443、8443、80、8080 这类常见端口，更容易伪装成正常网站流量。当然，选择其他端口也可以联通！**


<details>
  <summary>开源协议</summary>
  <pre><code> 
MIT License  |  维护者：Zhong Yuan
  </code></pre>
</details>

## 免责声明

- 本脚本仅供学习和测试，请勿用于非法用途。
- 作者不对使用此脚本可能造成的任何后果负责。

<details>
  <summary>致谢</summary>
  
- [Sing-Box](https://github.com/SagerNet/sing-box)
- 感谢[项目](https://github.com/Netflixxp/vlhy2)及其开发者，提供的技术支持与灵感参考。
- 所有为开源社区做出贡献的人
- [源本](https://github.com/shangguancaiyun/One-Click-Proxy-Installer)
- [副本](https://github.com/shangguan3366/One-Click-Proxy-Installer)

</details>
