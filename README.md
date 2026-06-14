# Klein-private-tool

## v2rayN routing rules

Rules file:

```text
v2rayn/klein-cn-service-direct.json
```

GitHub Raw URL:

```text
https://raw.githubusercontent.com/KleinCards/Klein-private-tool/main/v2rayn/klein-cn-service-direct.json
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

It intentionally does not include Windows process rules, such as `Weixin.exe`, `QQ.exe`, or `ToDesk.exe`, so the file stays portable across machines.

The selected service rule uses `geosite:*` references from the local v2rayN/Xray geosite database, plus a few manual `domain:*` entries. It does not add broad rules like `geosite:cn` or `geoip:cn`.

## Important private repo note

This repository is currently private. v2rayN usually cannot fetch a private GitHub Raw URL directly because it has no GitHub login/token context.

For one-click import from v2rayN, either:

- make this repository public, or
- copy the JSON file to a public GitHub repo/Gist/static host, or
- keep the repo private and use a local sync script with GitHub authentication.
