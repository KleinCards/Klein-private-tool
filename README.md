# Klein-private-tool

## v2rayN routing rules

Rules file:

```text
v2rayn/klein-cn-service-direct.json
```

Recommended import URL:

```text
https://github.com/KleinCards/Klein-private-tool/raw/refs/heads/main/v2rayn/klein-cn-service-direct.json
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
6. Direct selected Chinese services/domains
7. Final proxy fallback
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

It intentionally does not include Windows process rules, such as `Weixin.exe`, `QQ.exe`, or `ToDesk.exe`, so the file stays portable across machines.

It also does not add broad rules like `geosite:cn`, `geosite:geolocation-cn`, or `geoip:cn`.

## Public import status

This repository is public, and the URL above can be fetched without GitHub login. That means v2rayN should be able to import this rule file directly from the URL.
