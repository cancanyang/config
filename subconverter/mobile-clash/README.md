# Mobile Clash Subconverter Config

This directory stores a public external config for `subconverter`.

Use `mobile-clash-config.ini` as the `config=` parameter when generating a Clash/Mihomo profile for mobile clients such as Stash, Clash Meta for Android, or FlClash.

The config is intentionally strict:

- `proxy-groups` are generated from `custom_proxy_group=` entries in the INI.
- `rules` are generated from inline `ruleset=GROUP,[]RULE` entries in the INI.
- No third-party remote ruleset is expanded into the generated profile.
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
