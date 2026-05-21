# Mobile Clash Subconverter Config

This directory stores a public external config for `subconverter`.

Use `mobile-clash-config.ini` as the `config=` parameter when generating a Clash/Mihomo profile for mobile clients such as Stash, Clash Meta for Android, or FlClash.

The config is intentionally concise:

- `proxy-groups` are generated from `custom_proxy_group=` entries in the INI.
- `rules` are generated as compact `RULE-SET` / `GEOIP` / `MATCH` entries.
- Rule order follows common Clash/Mihomo practice: local/direct exceptions, blocking, specific services, broad proxy, China direct, `GEOIP,CN`, then `MATCH`.
- `rule-providers` are defined in `mobile-clash-base.yaml`.
- Custom editable providers live in `rules/`.
- `overwrite_original_rules=true` replaces rules from the original subscription.

Raw URL after pushing this repository:

```text
https://raw.githubusercontent.com/cancanyang/config/main/subconverter/mobile-clash/mobile-clash-config.ini
```

Example URL shape:

```text
http://YOUR_SUBCONVERTER_HOST:25500/sub?target=clash&url=YOUR_ENCODED_SUBSCRIPTION_URL&config=https%3A%2F%2Fraw.githubusercontent.com%2Fcancanyang%2Fconfig%2Fmain%2Fsubconverter%2Fmobile-clash%2Fmobile-clash-config.ini
```

Do not commit subscription URLs, server IPs, account tokens, or credentials to this repository.

## Files

- `mobile-clash-config.ini` - subconverter external config, policy groups and rule order.
- `mobile-clash-base.yaml` - Clash/Mihomo base profile containing `rule-providers`.
- `rules/custom-direct.yaml` - personal direct rules.
- `rules/custom-proxy.yaml` - personal proxy rules.
- `rules/custom-reject.yaml` - personal reject rules.
