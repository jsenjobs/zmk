# ZMK with Kim's PS/2 Mouse & Trackpoint Driver + Urob's Improvements

This branch includes the latest version of the PS/2 Mouse & Trackpoint driver.

You can [follow the comments in this zmk-config commit](https://github.com/infused-kim/zmk-config/commit/4134157ea054192bdc063ee4451ab780d7f01b8d) to figure out how to configure your PS/2 mouse or trackpoint.

You can also refer to the following PRs for more info:

- [ZMK PR #1751 - PS/2 Mouse & Trackpoint Driver](https://github.com/zmkfirmware/zmk/pull/1751)
- [Zephyr PR #15 - PS/2 driver using GPIO and UART](https://github.com/zmkfirmware/zephyr/pull/15))

If you have any questions, feel free to ask on the [zmk discord in #pointing-devices](https://discord.com/channels/719497620560543766/845285481888743434).

On top of that it contains the improvements from [the popular fork by urob](https://github.com/urob/zmk). You can [learn more about the benefits of his fork in his zmk-config](https://github.com/urob/zmk-config).

Due to the recent mouse code changes in zmk, it's based on the experimental zephyr 3.5 version, which may have bugs or stability issues. You can [learn more about it in this blog post draft](https://deploy-preview-1995--zmk.netlify.app/blog/2024/01/31/zephyr-3-5).

This is rebased with zmk/main as of 2024-01-16.

## Included features and PRs...

Below is a list of features currently included in the `main` branch _on top of_
the official ZMK master branch.

- **PS/2 Mouse & Trackpoint Driver** ([ZMK PR #1751](https://github.com/zmkfirmware/zmk/pull/1751) & [Zephyr PR #15](https://github.com/zmkfirmware/zephyr/pull/15))
- **Input Config - Auto toggle layer on mouse movement**
- **Mouse Keys using Zephyr 3.5** ([PR #2027](https://github.com/zmkfirmware/zmk/pull/2027) + [PR #1995](https://github.com/zmkfirmware/zmk/pull/1995))
- **swapper** (PR [#1366](https://github.com/zmkfirmware/zmk/pull/1366)) - official PR + fixes needed for Zephyr 3.2 and 3.5
- **smart-word** (PR [#1451](https://github.com/zmkfirmware/zmk/pull/1451)) - official PR, updated to Zephyr-3.2
- **fix-key-repeat** - fix [key-repeat rolling issue](https://github.com/zmkfirmware/zmk/issues/1207)
- **on-release-for-tap-preferred** - [on-release option for tap-preferred](https://github.com/celejewski/zmk/commit/d7a8482712d87963e59b74238667346221199293) by Andrzej
- **adv360pro** (PR [#1454](https://github.com/zmkfirmware/zmk/pull/1454)) - offical PR
- **zen-tweaks** - [display & battery improvements](https://github.com/caksoylar/zmk/tree/caksoylar/zen-v1%2Bv2) by Cem Aksoylar

Thanks and credits go out to krikun98, petejohanson and caksoylar for their work on the mouse keys code.

As well as to caksoylar for figuring out the changes needed for the swapper PR.

And of course to urob for his amazing fork.

## How to use it

You can [follow the comments in this zmk-config commit](https://github.com/infused-kim/zmk-config/commit/4134157ea054192bdc063ee4451ab780d7f01b8d) to figure out how to configure your PS/2 mouse or trackpoint.
