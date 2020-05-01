### 相对于原版的修改

增加 hide_candidate 配置，用于配置隐藏输入候选框。

此处非常感谢 [RIME](https://rime.im) [作者 lotem](https://github.com/lotem) 做出如此优秀的输入法，能兼容绝大部分输入方案。如今拼音输入法大行齐道的时候，相对小众的输入方案能后依托 RIME 实现很好的输入体验，窃以为双拼型码五笔才是中文输入的最佳方式。

### 为什么需要这个

修改起源于 [Squirrel #418](https://github.com/rime/squirrel/issues/418)。

为型码输入非常熟练的用户提供更加精简界面的输入法。多数型码输入如果存在重码的字词，在候选框中的顺序是不变的，当达到相当熟练的情况下，选词也无需用眼睛去看候选框。所以也就存在了不显示候选框这个需求。

***不推荐初中级熟练者使用***

### 如何使用

在 [Releases](https://github.com/JoneWang/squirrel/releases) 中下载最新的二进制包，并将 Squirrel 移动到『/Library/Input Methods』目录：

```bash
mv Squirrel.app /Library/Input\ Methods/
```

在输入设置中，中文输入添加 Squirrel 后即可使用（运行后可能会需要在安全设置中允许打开）。

***或手动编译安装***

clone 后，按[此流程编译安装](https://github.com/JoneWang/squirrel/blob/hide_candidate/INSTALL.md)。



打开 Squirrel 当前方案的配置文件，在 switches 中增加 hide_candidate，如下：

```yaml
switches:
  ...
  - name: hide_candidate
    reset: 1
```

然后 Deploy 后生效，此时输入文字时不会显示输入框，如需恢复，修改 reset 为 0 即可。


### 以下为原 Squirrel 描述

    鼠鬚管
    爲物雖微情不淺
    新詩醉墨時一揮
    別後寄我無辭遠
    
    　　——歐陽修

今由　[中州韻輸入法引擎／Rime Input Method Engine](https://rime.im)
及其他開源技術強力驅動

【鼠鬚管】輸入法
===
[![Download](https://api.bintray.com/packages/rime/squirrel/release/images/download.svg)](https://bintray.com/rime/squirrel/release/_latestVersion)
[![Build Status](https://travis-ci.org/rime/squirrel.svg)](https://travis-ci.org/rime/squirrel)
[![GitHub Tag](https://img.shields.io/github/tag/rime/squirrel.svg)](https://github.com/rime/squirrel)

式恕堂 版權所無

授權條款：[GPL v3](https://www.gnu.org/licenses/gpl-3.0.en.html)

項目主頁：[rime.im](https://rime.im)

您可能還需要 Rime 用於其他操作系統的發行版：

  * ibus-rime 及 fcitx-rime 用於 Linux
  * 【小狼毫】用於 Windows XP, Windows 7 ~ Windows 10

安裝輸入法
---

本品適用於 64 位 macOS 10.7+

初次安裝，如果在部份應用程序中打不出字，請註銷並重新登錄。

使用輸入法
---

選取輸入法指示器菜單裏的【ㄓ】字樣圖標，開始用鼠鬚管寫字。
通過快捷鍵 `` Ctrl+` `` 或 `F4` 呼出方案選單、切換輸入方式。

定製輸入法
---

定製方法，請參考線上 [幫助文檔](https://rime.im/docs/)。

使用系統輸入法菜單：

  * 選中「在線文檔」可打開以上網址
  * 編輯用戶設定後，選擇「重新部署」以令修改生效

安裝輸入方案
---

使用 [/plum/](https://github.com/rime/plum) 配置管理器獲取更多輸入方案。

致謝
---

輸入方案設計：

  * 【朙月拼音】系列

    感謝 CC-CEDICT、Android 拼音、新酷音、opencc 等開源項目

程序設計：

  * 佛振
  * Linghua Zhang
  * Chongyu Zhu
  * 雪齋
  * faberii
  * Chun-wei Kuo
  * Junlu Cheng
  * Jak Wings
  * xiehuc

美術：

  * 圖標設計 佛振、梁海、雨過之後
  * 配色方案 Aben、Chongyu Zhu、skoj、Superoutman、佛振、梁海

本品引用了以下開源軟件：

  * Boost C++ Libraries  (Boost Software License)
  * darts-clone  (New BSD License)
  * google-glog  (New BSD License)
  * Google Test  (New BSD License)
  * LevelDB  (New BSD License)
  * librime  (New BSD License)
  * OpenCC / 開放中文轉換  (Apache License 2.0)
  * plum / 東風破 (GNU Lesser General Public License 3.0)
  * Sparkle  (MIT License)
  * UTF8-CPP  (Boost Software License)
  * yaml-cpp  (MIT License)

感謝王公子捐贈開發用機。

問題與反饋
---

發現程序有 BUG，或建議，或感想，請反饋到
https://github.com/rime/home/issues

聯繫方式
---

技術交流，歡迎光臨 [Rime 代碼之家](https://github.com/rime/home)，
或致信 Rime 開發者 <rimeime@gmail.com>。

謝謝
