# LubanCat 通用 SDK（linux 分支）迁移到 LubanCatNext

基于 `lubancat_linux_generic.xml` 与 `remote.xml`，通用 SDK 所需仓库均来自 GitHub 组织 `LubanCatNext`。

## 已迁移组织

- GitHub Organization: `LubanCatNext`
- manifest 远端基地址：`https://github.com/LubanCatNext/`

## 通用清单需要的仓库

> 下面是 `repo init -m lubancat_linux_generic.xml` 会拉取的直接项目。

- `debian11`
- `debian12`
- `device_rockchip`
- `gcc-arm-10.3-2021.07-x86_64-aarch64-none-linux-gnu`
- `gcc-arm-10.3-2021.07-x86_64-arm-none-linux-gnueabihf`
- `kernel`（会检出到 `kernel-5.10` 与 `kernel-6.1` 两个路径）
- `lubancat-bin`
- `rkbin`
- `tools`
- `u-boot`
- `ubuntu20.04`
- `ubuntu22.04`

## 使用方式（可直接执行）

```bash
repo init -u https://github.com/LubanCatNext/manifests.git -b linux -m lubancat_linux_generic.xml
repo sync -c -j4
```

## 说明

- 项目 URL 规则：`https://github.com/LubanCatNext/<project-name>.git`。
- 当前仅覆盖“通用清单”范围，不包含专用/历史清单的全量迁移。
