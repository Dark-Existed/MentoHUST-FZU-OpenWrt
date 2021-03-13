# MentoHUST-FZU-OpenWrt

## ！！！未完工！！！

本项目由[MentoHUST-SYSU-OpenWrt](https://github.com/KumaTea/MentoHUST-SYSU-OpenWrt) 修改而来

# 使用方式

下载 (clone) 本项目至你的 OpenWrt 项目里的 `package` 下，建议新建一个 `custom` 文件夹并重命名该项目。完成后应该看起来像这样：

`<OpenWrt-DIR>/package/custom/mentohust`

然后再到 OpenWrt 根目录执行

```
./scripts/feeds update -a
./scripts/feeds install -a
make menuconfig
```

软件包位置在 `Network` - `Ruijie`
