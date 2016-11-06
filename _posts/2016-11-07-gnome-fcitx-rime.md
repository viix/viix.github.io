---
title:        "解决fcitx-rime中文输入法在gnome下不能切换及输入中文的问题"
# jekyll-seo-tag
description:  "solve the fcitx-rime doesn't work under gnome"
author:       "viix"
---

不久前的一天，我照例滚动我的arch，然后突然发现中文输入法坏了。一是无法使用ctrl-space切换，而是菜单切换到rime也无法输入中文。翻阅一些帖子，原来是因为新版本的gnome使用wayland，而fcitx可能支持不好。解决方法如下：

```
<!-- 在/etc/environment添加 --->
export GTK_IM_MODULE=fcitx
export QT_IM_MODULE=fcitx
export XMODIFIERS=@im=fcitx
```

done.
