# ZMK Firmware: Fork of urob's fork

This is my fork of urob's personal ZMK fork containing various experimental features. ~~It is regularly rebased
onto the latest upstream.~~

I made this fork while we wait for urob to update his.

This is rebased with zmk/main as of 2024-01-06.

## Included features and PRs...

Below is a list of features currently included in the `main` branch _on top of_
the official ZMK master branch.


> **Attention**
>
> This branch does not include the popular mouse keys PR.
>
> If you do want mouse key support, you can use the [urob/mouse branch](https://github.com/infused-kim/zmk/tree/urob/mouse), but it uses the highly experimental and potentially unstable zephyr 3.5 update.

- ~~**mouse** (PR [#778](https://github.com/zmkfirmware/zmk/pull/778)) - official PR + ftc's update + [update to Zephyr 3.2](https://github.com/urob/zmk/tree/mouse-3.2) + some safeguards + enforce hog device fix~~
- **swapper** (PR [#1366](https://github.com/zmkfirmware/zmk/pull/1366)) - official PR + fixes needed for Zephyr 3.2
- **smart-word** (PR [#1451](https://github.com/zmkfirmware/zmk/pull/1451)) - official PR, updated to Zephyr-3.2
- **fix-key-repeat** - fix [key-repeat rolling issue](https://github.com/zmkfirmware/zmk/issues/1207)
- **on-release-for-tap-preferred** - [on-release option for tap-preferred](https://github.com/celejewski/zmk/commit/d7a8482712d87963e59b74238667346221199293) by Andrzej
- **adv360pro** (PR [#1454](https://github.com/zmkfirmware/zmk/pull/1454)) - offical PR
- **zen-tweaks** - [display & battery improvements](https://github.com/caksoylar/zmk/tree/caksoylar/zen-v1%2Bv2) by Cem Aksoylar

Thanks to caksoylar for figuring out the changes needed for the swapper PR.

And of course to urob for his amazing fork.

## How to use it

### Github Actions

In order to use this branch with Github Actions, replace the contents of `west.yml` in
your `zmk-config/config` directory with the following contents:

```
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: urob
      url-base: https://github.com/urob
    - name: infused-kim
      url-base: https://github.com/infused-kim
  projects:
    - name: zmk
      remote: infused-kim
      revision: urob/no-mouse
      import: app/west.yml
  self:
    path: config
```
