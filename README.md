# Klein-private-tool

## v2rayN routing rules

Rules file:

```text
v2rayn/klein-cn-service-direct.json
```

Recommended import URL:

```text
https://github.com/KleinCards/Klein-private-tool/raw/main/v2rayn/klein-cn-service-direct.json
```

Use in v2rayN / V2RNY:

```text
Settings -> RoutingSetting -> Advanced Function -> Add -> URL(Optional)
```

Then import rules from the subscription URL.

## Rule intent

This rule set keeps the current Klein routing shape:

```text
1. Block UDP 443
2. Direct private LAN IP
3. Direct private LAN domains
4. Direct selected Chinese public DNS IPs
5. Direct selected Chinese public DNS domains
6. Direct selected Windows app processes
7. Direct selected Chinese services/domains
8. Final proxy fallback
```

The Windows app process rule currently covers WeChat, QQ, ToDesk, and WPS. The process names were checked against this machine's running process table and install directories:

```text
Weixin.exe
WeixinExt.exe
WeixinUpdate.exe
WeChatAppEx.exe
QQ.exe
QQEX.exe
ToDesk.exe
zagent.exe
CoreToolsMgrHelper.exe
wps.exe
wpp.exe
et.exe
wpspdf.exe
wpsofd.exe
wpsoffice.exe
wpscenter.exe
wpscloudlaunch.exe
wpscloudsvr.exe
wpslingxi.exe
promecefpluginhost.exe
ksolaunch.exe
ksomisc.exe
kwpswnsserver.exe
wpsupdate.exe
```

The selected service rule currently keeps only a small set of direct Chinese services:

```text
geosite:bilibili
geosite:category-collaborate-cn
geosite:tencent
geosite:wps
geosite:xiaohongshu
domain:gov.cn
```

It does not add broad rules like `geosite:cn`, `geosite:geolocation-cn`, or `geoip:cn`.

## Public import status

This repository is public, and the URL above can be fetched without GitHub login. That means v2rayN should be able to import this rule file directly from the URL.
