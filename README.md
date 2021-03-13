# MentoHUST-SYSU-OpenWrt

把[之前教程](https://kumatea.github.io/MentoHUST-SYSU-Guide/Guide.html)的编译步骤修改了下，现在可以在编译 OpenWrt 的时候安装了。

源码来自 @ivechan 的[mentohust的SYSU版本](https://github.com/ivechan/mentohust-SYSU)，移植方式参考了@KyleRicardo 的 [MentoHUST-OpenWrt-ipk包](https://github.com/KyleRicardo/MentoHUST-OpenWrt-ipk)，感谢。

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
