The reference layout analysis library built on top of keycat. 

# Upstream

Find the upstream repository here!

https://github.com/semilin/keymeow

# Changelog

```
2024-12-05  antlers  <antlers@illucid.net>

        Convert null bytes into replacement characters on import
        This reverts commit 62bc163cc1da2f3b008cff944a7ff0c6a182971e.

        I need it because I'm using `\uFFFD` to fill un-bound combos.

        I'm hoping that by processing null bytes into rcs on import I can use
        JSON nulls or null chars in my config.

        * src/lib.rs (LayoutData.flexible_from_keyboard_layout)
        (LayoutData.fixed_from_layout): Convert null bytes into replacement
        characters instead of dropping them.

2024-12-05  antlers  <antlers@illucid.net>

        Fork from Semi <3
        * Cargo.lock: semilin->antler5
        * Cargo.toml: semilin->antler5
```
