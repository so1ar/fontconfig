# fontconfig

自用 Linux 字体配置。

主要参考了[这篇文章](https://catcat.cc/post/2020-10-31/)以及作者自己的[配置文件](https://github.com/rydesun/dotfiles/tree/master/.config/fontconfig)，根据自己的使用情况做了些修改，个人使用的发行版是 Arch，其他发行版安装时包名可能不同。

- 主要使用字体：noto-fonts，安装了 [noto-fonts](https://archlinux.org/packages/extra/any/noto-fonts/) 和 [noto-fonts-cjk](https://archlinux.org/packages/extra/any/noto-fonts-cjk/)；

- 等宽字体：更纱黑体，安装 [ttf-sarasa-gothic](https://archlinux.org/packages/community/any/ttf-sarasa-gothic/)，更纱黑体的中文字型和 noto-fonts 的中文黑体字型其实都来自于思源黑体，所以事实上字型是没有区别的，但是 Arch 官方仓库打包的 noto-fonts-cjk 包的中文黑体字型缺少了一些变体，比如更多的字重和斜体，而更纱黑体是有多字重和斜体支持的，所以最终我还是选择了更纱黑体作为主要的等宽字体；

- 图标字体：nerd-fonts，安装 [ttf-nerd-fonts-mono](https://archlinux.org/packages/community/any/ttf-nerd-fonts-symbols-mono/)，作为等宽字体的 fallback 字体，这样无需为字体打补丁也可以用上图标字体，只需在对应软件的字体配置中指定为 monospace 即可；

- emoji 字体，iOS 风格的 emoji，安装 [ttf-apple-emoji](https://aur.archlinux.org/packages/ttf-apple-emoji)。

使用方法，安装对应字体后将 fontconfig 文件夹放入 `~/.config/` 目录即可，若想让字体配置全局生效而不是只对单用户生效，那就将 conf.d 文件夹中的几个 conf 文件放进 `/etc/fonts/conf.d`。
