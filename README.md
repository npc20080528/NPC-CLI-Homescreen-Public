> **中文跟英文的語意是一樣的，只是作者英文比較不好（非母語使用者），所以先寫中文的介紹，用翻譯翻成英文後，依我想表達的語意微調用字，擇一閱讀即可，若有衝突，則以中文為準。**
>
> **阿我看不太懂各種授權是什麼意思，就隨便設了一個，我的想法是檔案開源，非營利可以隨便用，若要營利請私訊作者討論細節。**
>
> **The Chinese and English versions convey the same meaning. The author is not a native English speaker, so the Chinese introduction was written first and then translated into English with minor wording adjustments to match the intended meaning. You only need to read one; if there are any conflicts, the Chinese version takes precedence.**
>
> **Oh, and I don't really understand what all the different licenses mean, so I just picked one at random. My intention is: the code is open-source, free for any non-commercial use; for commercial use, please DM the author to discuss the details.**

---

# NPC's CLI Homescreen

## 版本一覽 | Version Overview

| | **Min** | **Pro** | **Max** |
|---|---|---|---|
| APK 體積 | 38 KB | 82 KB | 16.4 MB |
| 安裝後 ROM 佔用 | 135 KB | 271 KB | 17.6 MB |
| dex2oat speed 後 | 367 KB | 767 KB | 64.9 MB |
| 支援 Android 版本 | 5 – 17 | 7 – 17 | 7 – 17 |
| 本地翻譯 | ✗ | ✗ | ✓ |

> **Pro 佔 Max 體積不到 1.2%**（767 / 64900 ≈ 0.0118）
> **Min 佔 Pro 體積不到 48%**（367 / 767 ≈ 0.4785）

---

<details>
<summary><b>📖 中文</b></summary>

<br>

<details>
<summary>程式起源與開發方式</summary>

<br>

用了很多款啟動器，都各有所長，但一直找不到完全符合我需求的，只好自己做一個。程式開發者是一個新手，程式能力不算太強，基本上都是提出構想之後叫AI寫，主要使用Arena AI agent mode。

</details>

---

<details>
<summary>程式簡介</summary>

<br>

目前仍有許多地區在取得高性能運算裝置方面較為困難，作者也是從小使用中低階手機長大的，時常受到市面上遍地皆是的巨型臃腫程式荼毒，也持續有記憶體(RAM)與儲存空間(ROM)不夠用的問題，直到近幾年條件較好才有能力買較高階手機做開發，深諳性能不足之苦，所以一開始我只做我需要的功能，將省電、無動畫的快速載入與刷新、極低的性能需求與RAM、ROM佔用做為程式的主要設計語言，且儘量提供多一點兼容性，務讓極低階手機仍有一戰之力，延長其使用壽命。後來越做越多功能，說好聽是集各家所長，但好像快把我手機上所有不用聯網的功能都做上去了😂。

總之所以後來要公開的時候，就分出了功能極致精簡的 **Min** 跟全功能的 **Max**，然後 Max 體積主要來自 translate 這個功能，所以如果想要 Max 的豐富功能，又想要極致輕量化的體積，沒有本地翻譯功能的 **Pro** 就應運而生。

> 原本在安卓原生程式需要十數 GB 體積的功能，最後在我的濃縮下只要不到 65 MB⁽¹⁾。另外，如果你不需要本地翻譯，不到 800 KB 的 Pro⁽²⁾ 功能多樣性與完整性絕對超乎你的想像，若你只想要極小體積，也用不太到 Pro 的各種複雜功能，則可以選擇 Min，體積可再減超過一半⁽⁴⁾。如只需要部份 Pro 功能，又想要榨出每一分空間，可自行抓取原始碼做出各種功能排列組合的版本，若能力較弱，亦可誠心求取作者的幫助。（看情況幫，作者時間有限，希望不要太多請求）

**備註：**

⁽¹⁾⁽²⁾ 經作者實測，Min、Pro、Max 的 APK 體積分別是 38KB、82KB、16.4MB，下載後未使用的 ROM 佔用分別為 135KB、271KB、17.6MB，Max 下載本地 translate 包後，程式 ROM 佔用為 60.9MB（約 43.2MB 的包在我手機上被當快取），用 termux 將本程式的 dex2oat 改成 speed 之後，程式 ROM 佔用分別為 367KB、767KB、64.9MB，正常使用情境（speed-profile）下應介於兩者之間，實際大小因實際使用情境與不同裝置版本而有差異，應以實際體驗為準。

⁽³⁾ 767 / 64900 = 0.01181818...

⁽⁴⁾ 367 / 767 = 0.478487614...

</details>

---

<details>
<summary>這個程式對我來說的意義</summary>

<br>

這個程式大概取代了我手機的約 15 個 app，每個 app 都是我精挑細選的，大概能覆蓋一般的 5 個程式，所以總體來說本程式大概等於市面上近百個普通的臃腫程式，原本這些 app 已經大幅提升了我的生產力與使用效率，只是功能太分散，有些也過於臃腫，在整合了之後，依我的邏輯精簡的互動，再搭配 alias，更是讓我使用手機的效率大幅提升，只是不確定能不能賺回我用來開發的程式的時間就是了，但至少我在其中獲得了樂趣，有時也能確保我拿起手機卻打開了原本非預期開啟的程式。在公開之後，我也希望能幫助低性能安卓手機延長使用壽命，或是讓追求與眾不同的極客們多一點選擇與啟發（好像有點太有自信😂）。

</details>

---

<details>
<summary>指令列表與簡介</summary>

<br>

> Pro 與 Max 只列出相對 Min 與 Pro 的**新增指令**，相同功能不重複列出。
> 完整指令亦可以在程式內使用 `help` 指令查詢，詳細功能以實際使用為準。

### 指令樹狀總覽

```
NPC's CLI Homescreen
├── Min（基礎指令）
│   ├── alias          — 別名管理
│   ├── <app name>     — 啟動 app
│   ├── apps           — 列出已安裝 app
│   ├── help           — 顯示指令列表
│   ├── rm             — 刪除項目
│   ├── status         — 系統狀態（唯讀）
│   ├── color          — 顏色設定
│   ├── fontsize       — 字體大小
│   └── toptext        — 頂部文字
│
├── Pro（在 Min 基礎上新增）
│   ├── 一般指令
│   │   ├── accessibility  — 無障礙功能列表
│   │   ├── AOD            — 全螢幕時鐘/計時器/碼錶
│   │   ├── BPM            — 節拍器
│   │   ├── calc / calcs   — 計算機 / 計算歷史
│   │   ├── compass        — 羅盤
│   │   ├── <date>         — 星期 & 農曆查詢
│   │   ├── flash          — 手電筒
│   │   ├── gestures       — 手勢列表
│   │   ├── jot / jotting / jottings — 筆記
│   │   ├── map / playstore / trans / yt — 應用內搜尋
│   │   ├── music / musics — 本地音樂播放
│   │   ├── rec / recs     — 錄音
│   │   ├── rm             — 刪除（擴充更多項目）
│   │   ├── search         — 搜尋引擎
│   │   ├── settings       — 設定列表
│   │   └── status         — 系統狀態（亮度 & 音量可調）
│   │
│   ├── 無障礙指令（需開啟系統無障礙服務）
│   │   ├── back / home / recents   — 導航按鈕
│   │   ├── quicksettings / statusbar — 面板操作
│   │   ├── trigger / triggers       — 按鍵觸發
│   │   ├── wait                     — 延時
│   │   ├── vibrate                  — 震動
│   │   └── x<n> y<n>               — 螢幕點擊
│   │
│   └── 設定項目
│       ├── addtimems / batterystyle / history
│       ├── holdtime / max2tapgap
│       ├── musicautooff / musicfolder / recfolder
│       ├── refreshspeed / swipepx / tempunit
│       ├── toptextshow
│       └── AOD 相關（AODcolor / AODmax2tapgap / TMFS / TMFSgap / TMVB ...）
│
└── Max（在 Pro 基礎上新增）
    └── translate      — 本地翻譯（Google ML Kit）
```

---

<details>
<summary>&emsp;📋 Min 指令詳細</summary>

<br>

```
alias               — 列出所有別名，或 alias <name> <command> 設定別名（用 ; 設定多個）
alias <name>        — 查看單一別名
<app name>          — 啟動 app（使用完整名稱）
apps                — 列出已安裝的 app
help                — 顯示指令列表
rm <alias|toptext>  — 刪除項目
status              — 顯示 date time battery device ram rom temp bright vol
                      wifi data bluetooth gps flash version
                      輸入單一項目名稱可個別查詢（僅檢視）
color (above|below|background)
                    — 用 Hex 色碼修改上方、下方、背景顏色
                      預設 #FFFFFF | #00FF00 | #000000
fontsize            — 修改文字大小，範圍 8-40 的正整數，預設 18
toptext <text|status item>
                    — 用 ; 分隔項目，| 開頭為換行續行，;; 強制換行
```

</details>

<details>
<summary>&emsp;📋 Pro 指令詳細</summary>

<br>

<details>
<summary>&emsp;&emsp;一般指令 (help)</summary>

<br>

```
accessibility           — 列出所有無障礙功能與說明
                          （需在系統無障礙設定中啟用「NPC's CLI Homescreen」）
AOD                     — 顯示全螢幕時鐘 / 計時器 / 碼錶
BPM <非負整數>           — 啟動節拍器；BPM 0 停止
calc <expression>       — 計算機（powered by exp4j）
calcs                   — 顯示計算歷史
compass                 — 顯示當前方位（角度 + 16 方位）
<date>                  — 顯示該日星期（15821015-99991231）
                          及農曆日期（20260217-20560214）
flash                   — 顯示手電筒狀態；加 [on|1|off|0|toggle|-1] 切換
gestures                — 顯示所有手勢及其指令
jot <name> <content>    — 寫筆記
jotting <name>          — 查看筆記
jottings                — 列出所有筆記及內容
map|playstore|trans|yt <keyword>
                        — 在對應 app 內搜尋，無 app 則用網頁版
music                   — 顯示播放狀態；加 [on|1|off|0|toggle|-1] 播放
                          輸入 prev / next 切換曲目
musics                  — 列出本地音訊檔，輸入數字播放
rec [on|1|off|0|toggle|-1]
                        — 錄音
recs                    — 列出錄音檔，輸入數字播放
rm <item>               — 刪除項目
                          （alias|calcs|gesture|history|jotting|toptext）
search <keyword>        — 用預設引擎搜尋（URL 直接開啟）
settings                — 列出所有設定
status                  — 同 Min，但亮度與音量可調整
                          其它可透過 alias + accessibility 調整
```

</details>

<details>
<summary>&emsp;&emsp;無障礙指令 (accessibility)</summary>

<br>

```
back            — 按下返回鍵
home            — 按下主頁鍵
quicksettings   — 開啟快速設定面板
recents         — 開啟最近應用程式
statusbar       — 展開通知列
trigger         — 監聽按鍵，設定 tap / 2tap / hold 指令
triggers        — 列出所有按鍵，可全部開啟或關閉
wait            — 在下一個指令前暫停指定時間（用 ; 分隔指令）
vibrate         — 加入震動，可作為腳本提醒
x<number> y<number>
                — 點擊螢幕指定座標
```

</details>

<details>
<summary>&emsp;&emsp;設定項目 (settings)</summary>

<br>

**一般設定：**

| 設定項 | 說明 | 預設值 |
|---|---|---|
| `addtimems` | status 的 time 加入三位毫秒（不太準，僅供參考） | off |
| `batterystyle` | 電量顯示：`num`（數字）/ `mix`（實心+空心方塊）/ `sol`（僅實心方塊），可自訂總格數 | — |
| `history` | 以 txt 檔記錄使用者輸入歷史 | off |
| `holdtime` | 長按判定時間 | 500ms |
| `max2tapgap` | 雙擊最大間隔 | 300ms |
| `musicautooff` | 自動停止本地音樂：`always`（無藍牙音訊裝置時）/ `auto`（藍牙從開→關時）/ `none`（從不） | auto |
| `musicfolder` | 本地音樂讀取資料夾 | — |
| `recfolder` | 錄音檔存放資料夾 | — |
| `refreshspeed` | 刷新時間：`time` / `compass` / `other` | 1000ms / 500ms / 1s |
| `swipepx` | 滑動判定距離 | 105 |
| `tempunit` | 溫度單位 | °C |
| `toptextshow` | 播放時顯示在 toptext：`music` / `rec` / `bpm` | 全部 on |

**AOD 設定：**

| 設定項 | 說明 | 預設值 |
|---|---|---|
| `AOD holdtime` | AOD 長按判定時間 | 500ms |
| `AODcolor` | `number` / `background` 顏色 | #00FF00 / #000000 |
| `AODmax2tapgap` | AOD 雙擊最大間隔 | 300ms |
| `TMFS` (timerflash) | 計時器閃爍次數 | 3 |
| `TMFSgap` (timerflashgap) | 閃爍間隔（0 = 閃爍時間等於震動時間；不要閃爍請設 TMFS 為 0） | 0ms |
| `TMVB` (timervibrate) | 計時器震動時間 | 1000ms |

</details>

</details>

<details>
<summary>&emsp;📋 Max 指令詳細</summary>

<br>

```
translate — 本地翻譯（powered by Google ML Kit）
```

</details>

</details>

---

<details>
<summary>權限需求</summary>

<br>

> 不同意也可以，只是需要該權限的功能將無法使用。

### Min

| 權限 | 用途 |
|---|---|
| 偵測附近裝置 | 讀取 Wi-Fi 與藍牙狀態（好像不同意也能偵測🤔） |

### Pro（相對 Min 新增）

| 權限 | 用途 |
|---|---|
| 讀取裝置檔案 | music 與 rec 功能的讀寫 |
| 通知 | 新版 Android 要求可錄音/播放音訊的程式提供通知 |
| 麥克風 | 錄音功能 |
| 調整設定 | 調整裝置亮度與音量 |
| 震動 | AOD timer 預設震動；accessibility 的 vibrate 指令 |
| 無障礙 | 僅無障礙功能需要 |

### Max（相對 Pro 新增）

| 權限 | 用途 |
|---|---|
| 網路 | 下載本地翻譯包（其它地方用不到） |

</details>

---

<details>
<summary>目前已知問題</summary>

<br>

1. 音量鍵設 trigger 之後，就算把動作改成調整音量，非處於播放音樂時，無法依靠音量鍵調整音量。

</details>

---

<details>
<summary>不同安卓版本差異</summary>

<br>

| Android 版本 | 差異 |
|---|---|
| **≤ 11** | 短於 1 秒的錄音會直接丟棄（無內建垃圾桶） |
| **≤ 10** | 無法編碼 Opus，改用 AMR-WB（3GP 封裝）錄音，但仍有 VOICE_COMMUNICATION 模式的 AEC + NS + AGC 三重降噪。Android 10 以上使用 Ogg/Opus，僅差在儲存效率 |
| **近幾代** | 權限監管變嚴，需額外授權，但給滿權限即無差異 |

</details>

---

<details>
<summary>目前考慮過的功能</summary>

<br>

<details>
<summary>&emsp;1. 多語言</summary>

<br>

雖然作者是中文母語使用者，且英文超爛🤡，早期版本曾經想要做多語言，從英文、繁體中文、簡體中文開始，之後再看還有什麼需求，但後來功能越做越多，越做越複雜，有些指令翻成中文會變得挺複雜的，甚至有些我根本不知道怎麼翻💀，加上還要寫一堆映射指令，會大幅增加程式體積，也會降低運行效率，所以為了極致的效率，最後還是決定全英文，這個功能作者是不會更新的。

</details>

<details>
<summary>&emsp;2. 修改 jottings 存放位置</summary>

<br>

就像 musicfolder、recfolder 一樣，作者曾經做過 jottingsfolder，但不論我怎麼試，程式改了幾次，都讀不到這個程式的 txt 檔案，後來就放棄了，坐等大神指點迷津。

</details>

<details>
<summary>&emsp;3. 簡單的離線遊戲</summary>

<br>

像是貪食蛇、俄羅斯方塊之類的遊戲，在這個 CLI 界面可以很好的呈現，但作者不玩遊戲，做出來頂多玩一下就放著生灰了，遊戲內判斷的指令也不少，我有預感如果要統一設計語言，我會 debug 到崩潰，然後還是一樣有增加體積的問題，目前暫時不考慮更新。

</details>

<details>
<summary>&emsp;4. 本地 PDF 檔案閱讀</summary>

<br>

我曾使用我從 2024 年開始關注，程式製作當時剛發布（2026 年 8 月 27 日發布）Android Jetpack PDF Viewer 模組（androidx.pdf）Beta 版（1.0.0-beta01），但不知為何 debug 了好幾個版本，不是當掉就是閃退，心態崩了，直接棄更這個功能，一樣求大神指路😭

</details>

<details>
<summary>&emsp;5. 更好的兼容性</summary>

<br>

從原本只支援安卓 16，到目前已經拓展到 Min 支援安卓 5-17，Pro 與 Max 支援安卓 7-17，原本 AI 有給我 v7a、v8a、X86、X86-64，最後我為了極小體積，加上我的初衷是為手機提供服務，最後只保留 v8a。

- **X86：** 可以輕鬆跑 Linux，其中有很多我覺得比我的程式更好用的分支版本，而且是真正的 CLI（安卓運行時，看似表面是 CLI，但實際運算與渲染的邏輯還是維持在十分耗電的 GUI），如果還是覺得不好用的人，程度應該足以用 LFS（Linux From Scratch）自己做了。
- **手機生態：** 近幾年連幾個比較開放的手機廠商都越來越難 root，只能維持在安卓原生版本的情況下，我覺得目前手機在這方面有產品斷層與空洞。
- **iOS：** 蘋果的權限控制好像比較複雜，抱歉了 iPhone 用戶🥺，我曾經是有想讓你們可以用的，看未來生態能不能開放一點吧！

</details>

<details>
<summary>&emsp;6. 用 API 抓天氣跟雲端 AI</summary>

<br>

優點是在做到相同甚至更多、更好的功能的情況下，同時維持極小體積，缺點是需要網路，本來是想說做完全不需要網路的功能，但真的挺吸引人的，目前正以 Pro 為基礎的 Dev（未公開）測試中，先嘗試了 Groq 跟中央氣象署的 API，還有什麼實用的 API 想推薦，或是想玩玩看 Dev 都可以私訊作者。

</details>

<details>
<summary>&emsp;7. 取得 ADB 權限</summary>

<br>

這個超讚，成功之後可以取代部份 Termux 功能，trigger 也能設定除了音量鍵以外的按鈕，但也是一樣做了好幾個版本之後一直沒有成功，如果需要這個功能的，我原本是用 Key Mapper，推薦給你。雖然失敗了，但我還是覺得這個功能挺實用的，之後有空還是會考慮再嘗試看看，如果有大神願意幫忙，感激不盡。

</details>

<details>
<summary>&emsp;8. triggers 排列組合形成新指令</summary>

<br>

目前問題是不好命名，目前音量鍵兩個，排列組合只要設兩種，但有些手機物理按鈕超多，排列組合是比指數快很多的階乘，兼具易讀性與極簡的命名很難找，不喜歡 Key Mapper 那種 trigger 1：（動作 1）、（動作 2）的這種，而且參數調整不好時，指令間容易相互干擾，不適合一般人使用，未來會考慮在 Dev 做做看，但應該不會發布在公開版本。

</details>

</details>

---

<details>
<summary>開發者招募與聯絡方式</summary>

<br>

### 加入條件

1. 對 Pro 的功能瞭若指掌
2. 嚴格的背景審查
3. 具有程式開發經驗或具程式邏輯

> 希望能有一些專業人士加入，因為關於 API 的額度管理我想朝去中心化的方向製作。

### 開發資訊

本程式經歷了約 **30 天**開發、**105 個版本**更新，修正與微調了**上萬個細節**。若需要版本更新日誌或歷史版本的原始碼或 APK 做研究，請聯繫作者。如本程式出現了 bug 或界面不夠直覺的地方，或是對本程式有任何建議與疑問，也歡迎聯繫作者討論。

### 聯絡方式

📧 **Email：** fanpao757@gmail.com

> 先用 Email 聯絡，如果有必要或是通過了 Dev 審核，我才會給私人聯絡方式。

</details>

</details>

---

---

<details>
<summary><b>📖 English</b></summary>

<br>

<details>
<summary>Origin and Development Approach</summary>

<br>

I've tried many launchers, each with its own strengths, but I could never find one that fully met my needs, so I decided to build my own. The developer is a beginner with modest programming skills; basically, I come up with ideas and have AI write the code, primarily using Arena AI agent mode.

</details>

---

<details>
<summary>Program Overview</summary>

<br>

There are still many regions where obtaining high-performance computing devices remains difficult. The author also grew up using low- to mid-range phones, constantly plagued by the bloated, oversized apps that are everywhere on the market, and perpetually struggling with insufficient memory (RAM) and storage (ROM). It wasn't until recent years, when my circumstances improved, that I could afford a higher-end phone for development. Having deeply experienced the pain of inadequate performance, I initially only built the features I needed, making power efficiency, animation-free fast loading and refreshing, and extremely low demands on performance, RAM, and ROM the core design principles of the app. I also tried to provide as much compatibility as possible, ensuring that even very low-end phones could still hold their own and extend their usable lifespan. Later, I kept adding more and more features — to put it nicely, I gathered the best of all worlds, but it feels like I've basically crammed every offline function from all the apps on my phone into this one 😂.

Anyway, when it came time to release it publicly, I split it into an ultra-minimalist **Min** and a full-featured **Max**. The bulk of Max's size comes from the translate feature, so for those who want the rich functionality of Max but also want an ultra-lightweight footprint, **Pro** — a Max without local translation — was born.

> Features that would normally require over ten GB in a native Android app were condensed by me down to under 65 MB⁽¹⁾. Additionally, if you don't need local translation, Pro⁽²⁾ at under 800 KB offers a diversity and completeness of features that will absolutely exceed your expectations. If you only want an extremely small footprint and don't really need the various complex features of Pro, you can choose Min, which reduces the size by more than half again⁽⁴⁾. If you only need some of Pro's features and want to squeeze out every last byte of space, you can grab the source code and build your own variant with any combination of features. If your skills are limited, you're also welcome to sincerely ask the author for help. (Help is provided on a case-by-case basis; the author's time is limited, so please don't send too many requests.)

**Notes:**

⁽¹⁾⁽²⁾ Based on the author's actual testing, the APK sizes of Min, Pro, and Max are 38 KB, 82 KB, and 16.4 MB respectively. After installation (unused), ROM usage is 135 KB, 271 KB, and 17.6 MB respectively. After Max downloads the local translate package, the app's ROM usage is 60.9 MB (the ~43.2 MB package is treated as cache on my phone). After using Termux to change this app's dex2oat mode to "speed," ROM usage becomes 367 KB, 767 KB, and 64.9 MB respectively. Under normal usage conditions (speed-profile), it should fall somewhere between these two extremes. Actual sizes vary depending on real usage scenarios and different device versions, so actual experience should be the reference.

⁽³⁾ 767 / 64900 = 0.01181818...

⁽⁴⁾ 367 / 767 = 0.478487614...

</details>

---

<details>
<summary>What This App Means to Me</summary>

<br>

This app has replaced roughly 15 apps on my phone, each of which I carefully hand-picked. Each of those apps could generally cover about 5 ordinary apps, so overall, this single app is roughly equivalent to nearly a hundred typical bloated apps on the market. Those original apps had already significantly boosted my productivity and efficiency, but their features were too scattered and some were overly bloated. After integrating them, streamlining the interactions according to my own logic, and pairing everything with aliases, my phone usage efficiency has improved dramatically. I'm just not sure if I'll ever recoup the time I spent developing it, but at least I had fun in the process, and sometimes it even ensures that when I pick up my phone, I don't accidentally open an app I didn't intend to. Now that it's public, I also hope it can help extend the lifespan of low-performance Android phones, or give geeks who seek something different a few more options and some inspiration (maybe a bit too confident of me 😂).

</details>

---

<details>
<summary>Command List and Brief Descriptions</summary>

<br>

> For Pro and Max, only commands **new** relative to Min and Pro are listed; identical features are not repeated.
> The full command list can also be queried within the app using the `help` command. Detailed functionality is subject to actual use.

### Command Tree Overview

```
NPC's CLI Homescreen
├── Min (Base Commands)
│   ├── alias          — alias management
│   ├── <app name>     — launch an app
│   ├── apps           — list installed apps
│   ├── help           — show command list
│   ├── rm             — delete item
│   ├── status         — system status (read-only)
│   ├── color          — color settings
│   ├── fontsize       — font size
│   └── toptext        — top text
│
├── Pro (Added on top of Min)
│   ├── General Commands
│   │   ├── accessibility  — accessibility feature list
│   │   ├── AOD            — full-screen clock / timer / stopwatch
│   │   ├── BPM            — metronome
│   │   ├── calc / calcs   — calculator / history
│   │   ├── compass        — compass
│   │   ├── <date>         — weekday & lunar date lookup
│   │   ├── flash          — flashlight
│   │   ├── gestures       — gesture list
│   │   ├── jot / jotting / jottings — notes
│   │   ├── map / playstore / trans / yt — in-app search
│   │   ├── music / musics — local music playback
│   │   ├── rec / recs     — voice recording
│   │   ├── rm             — delete (expanded items)
│   │   ├── search         — search engine
│   │   ├── settings       — settings list
│   │   └── status         — system status (brightness & volume adjustable)
│   │
│   ├── Accessibility Commands (requires system accessibility service)
│   │   ├── back / home / recents   — navigation buttons
│   │   ├── quicksettings / statusbar — panel controls
│   │   ├── trigger / triggers       — key triggers
│   │   ├── wait                     — delay
│   │   ├── vibrate                  — vibration
│   │   └── x<n> y<n>               — screen tap
│   │
│   └── Settings
│       ├── addtimems / batterystyle / history
│       ├── holdtime / max2tapgap
│       ├── musicautooff / musicfolder / recfolder
│       ├── refreshspeed / swipepx / tempunit
│       ├── toptextshow
│       └── AOD-related (AODcolor / AODmax2tapgap / TMFS / TMFSgap / TMVB ...)
│
└── Max (Added on top of Pro)
    └── translate      — local translation (Google ML Kit)
```

---

<details>
<summary>&emsp;📋 Min Command Details</summary>

<br>

```
alias               — list all aliases, or alias <name> <command> to set (use ; for multiple)
alias <name>        — view one alias
<app name>          — launch an app (use exact name)
apps                — list installed apps
help                — show this list
rm <alias|toptext>  — delete item
status              — show date time battery device ram rom temp bright vol
                      wifi data bluetooth gps flash version
                      enter an item name to check individually (view only)
color (above|below|background)
                    — use hex color codes to modify top, bottom, background colors
                      defaults: #FFFFFF | #00FF00 | #000000
fontsize            — modify text display size, range 8-40 (positive integer), default 18
toptext <text|status item>
                    — separate items with ;, | for continuation lines, ;; for forced line break
```

</details>

<details>
<summary>&emsp;📋 Pro Command Details</summary>

<br>

<details>
<summary>&emsp;&emsp;General Commands (help)</summary>

<br>

```
accessibility           — list all accessibility features and explanations
                          (enable "NPC's CLI Homescreen" in system accessibility settings)
AOD                     — show full-screen clock / timer / stopwatch
BPM <non-negative int>  — start metronome; BPM 0 stops it
calc <expression>       — calculator (powered by exp4j)
calcs                   — show calculation history
compass                 — show current heading (degrees + 16-point direction)
<date>                  — show weekday (15821015-99991231)
                          and lunar date (20260217-20560214)
flash                   — show torch state; add [on|1|off|0|toggle|-1] to switch
gestures                — show all gestures and their commands
jot <name> <content>    — write a note
jotting <name>          — view a note
jottings                — list all notes and contents
map|playstore|trans|yt <keyword>
                        — search inside that app, web version as fallback
music                   — show playback; add [on|1|off|0|toggle|-1] to play
                          input prev / next to switch tracks
musics                  — list local audio files, type a number to play
rec [on|1|off|0|toggle|-1]
                        — record voice
recs                    — list recordings, type a number to play
rm <item>               — delete item
                          (alias|calcs|gesture|history|jotting|toptext)
search <keyword>        — search with default engine (URL opens directly)
settings                — list all settings
status                  — same as Min, but brightness & volume are adjustable
                          others can be adjusted via custom aliases + accessibility
```

</details>

<details>
<summary>&emsp;&emsp;Accessibility Commands</summary>

<br>

```
back            — press the back button
home            — press the home button
quicksettings   — open the quick-settings panel
recents         — open the recent apps overview
statusbar       — expand the notification shade
trigger         — listen for a pressed key, assign tap/2tap/hold commands
triggers        — list every key, switch them all on or off
wait            — pause before the next command (; separates commands)
vibrate         — add vibration to scripts as a reminder
x<number> y<number>
                — tap the screen at that point
```

</details>

<details>
<summary>&emsp;&emsp;Settings</summary>

<br>

**General Settings:**

| Setting | Description | Default |
|---|---|---|
| `addtimems` | Add 3-digit milliseconds to status time (not very accurate, rough reference) | off |
| `batterystyle` | Battery display: `num` (numeric) / `mix` (filled + hollow blocks) / `sol` (filled only); total blocks customizable | — |
| `history` | Record user input history in a txt file | off |
| `holdtime` | Hold detection time | 500ms |
| `max2tapgap` | Maximum double-tap gap | 300ms |
| `musicautooff` | Auto-stop local music: `always` (no BT audio device) / `auto` (BT on→off) / `none` (never) | auto |
| `musicfolder` | Local music folder | — |
| `recfolder` | Recording storage folder | — |
| `refreshspeed` | Refresh interval: `time` / `compass` / `other` | 1000ms / 500ms / 1s |
| `swipepx` | Swipe detection distance | 105 |
| `tempunit` | Temperature unit | °C |
| `toptextshow` | Show in toptext when playing: `music` / `rec` / `bpm` | all on |

**AOD Settings:**

| Setting | Description | Default |
|---|---|---|
| `AOD holdtime` | AOD hold detection time | 500ms |
| `AODcolor` | `number` / `background` color | #00FF00 / #000000 |
| `AODmax2tapgap` | AOD max double-tap gap | 300ms |
| `TMFS` (timerflash) | Timer flash count | 3 |
| `TMFSgap` (timerflashgap) | Flash gap (0 = flash duration equals vibration; set TMFS to 0 for no flash) | 0ms |
| `TMVB` (timervibrate) | Timer vibration duration | 1000ms |

</details>

</details>

<details>
<summary>&emsp;📋 Max Command Details</summary>

<br>

```
translate — local translation (powered by Google ML Kit)
```

</details>

</details>

---

<details>
<summary>Permission Requirements</summary>

<br>

> You can decline them, but features requiring those permissions won't be available.

### Min

| Permission | Purpose |
|---|---|
| Detect nearby devices | Read Wi-Fi and Bluetooth status (seems to work even if declined 🤔) |

### Pro (added beyond Min)

| Permission | Purpose |
|---|---|
| Read device files | Reading and writing for music and rec features |
| Notifications | Required on newer Android for apps that record/play audio |
| Microphone | Recording feature |
| Adjust settings | Adjust device brightness and volume |
| Vibration | AOD timer default vibration; accessibility vibrate command |
| Accessibility | Only for accessibility features |

### Max (added beyond Pro)

| Permission | Purpose |
|---|---|
| Network | Downloading local translation package (not used elsewhere) |

</details>

---

<details>
<summary>Currently Known Issues</summary>

<br>

1. After setting a volume key as a trigger, even if the action is changed to adjust volume, the volume keys cannot adjust the volume when music is not playing.

</details>

---

<details>
<summary>Differences Across Android Versions</summary>

<br>

| Android Version | Difference |
|---|---|
| **≤ 11** | Recordings shorter than 1 second are permanently deleted (no built-in trash bin) |
| **≤ 10** | Cannot encode Opus; uses AMR-WB (3GP container) instead, but still has VOICE_COMMUNICATION mode with AEC + NS + AGC triple noise reduction. Android 10+ uses Ogg/Opus; only differs in storage efficiency |
| **Recent versions** | Stricter permission controls; additional permissions needed, but no functional differences when all permissions are granted |

</details>

---

<details>
<summary>Features I've Considered</summary>

<br>

<details>
<summary>&emsp;1. Multi-language support</summary>

<br>

Although the author is a native Chinese speaker with terrible English 🤡, early versions once aimed to support multiple languages, starting with English, Traditional Chinese, and Simplified Chinese, then expanding based on demand. However, as features grew more numerous and complex, some commands became quite complicated to translate into Chinese, and some I honestly have no idea how to translate 💀. On top of that, writing a bunch of mapped commands would significantly increase the app size and reduce runtime efficiency. So, in the pursuit of ultimate efficiency, I ultimately decided to keep everything in English. The author will not be updating this feature.

</details>

<details>
<summary>&emsp;2. Changing the jottings storage location</summary>

<br>

Just like musicfolder and recfolder, the author once implemented a jottingsfolder, but no matter how I tried or how many times I rewrote the code, the app couldn't read its own txt files from that location. I eventually gave up and am waiting for an expert to point me in the right direction.

</details>

<details>
<summary>&emsp;3. Simple offline games</summary>

<br>

Games like Snake or Tetris could be nicely rendered in this CLI interface. However, the author doesn't play games, so at best I'd play for a bit and then let it gather dust. The in-game logic commands are also quite numerous, and I have a feeling that if I tried to unify the design language, I'd debug myself into a breakdown. Plus, there's the same issue of increased app size. Not considering this for now.

</details>

<details>
<summary>&emsp;4. Local PDF file reading</summary>

<br>

I tried using the Android Jetpack PDF Viewer module (androidx.pdf) Beta (1.0.0-beta01), which I had been following since 2024 and which was just released (August 27, 2026) around the time I was building the app. But for some reason, after debugging through several versions, it either froze or crashed. I lost my sanity and abandoned this feature entirely. Once again, begging for an expert's guidance 😭

</details>

<details>
<summary>&emsp;5. Better compatibility</summary>

<br>

Starting from supporting only Android 16, the app has now expanded to support Android 5–17 for Min, and Android 7–17 for Pro and Max. Originally, the AI gave me builds for v7a, v8a, x86, and x86-64, but in the end, to keep the size as small as possible and since my original intention was to serve phones, I kept only v8a.

- **x86:** Can easily run Linux, which has many forked distributions that I think are better than my app, and they're true CLI (when running on Android, the surface may look like CLI, but the actual computation and rendering logic still operates within the very power-hungry GUI). Those who still find those unsatisfactory should have enough skill to build their own with LFS (Linux From Scratch).
- **Phone ecosystem:** In recent years, even the more open phone manufacturers have made rooting increasingly difficult. Under the constraint of staying on stock Android, I feel there's currently a product gap and void in this area.
- **iOS:** Apple's permission controls seem quite complex. Sorry, iPhone users 🥺 — I did once want to make this available to you. Let's see if the ecosystem opens up a bit in the future!

</details>

<details>
<summary>&emsp;6. Using APIs for weather and cloud AI</summary>

<br>

The advantage is achieving the same or even more and better features while maintaining an ultra-small footprint. The downside is that it requires an internet connection. I originally intended to build a completely offline app, but this is really quite appealing. Currently being tested in a Dev (unreleased) build based on Pro. I've tried the Groq and Central Weather Administration APIs so far. If you have any useful APIs to recommend or want to try out Dev, feel free to DM the author.

</details>

<details>
<summary>&emsp;7. Obtaining ADB permissions</summary>

<br>

This one is amazing — if successful, it could replace part of Termux's functionality, and triggers could be set for buttons other than the volume keys. But similarly, after several iterations, I never got it working. If you need this feature, I originally used Key Mapper — recommended. Although I failed, I still think this feature is quite practical, so I might try again when I have time. If any experts are willing to help, I'd be extremely grateful.

</details>

<details>
<summary>&emsp;8. Combining triggers to form new commands</summary>

<br>

The current problem is that they're hard to name. With just two volume keys, only two combinations need to be defined, but some phones have tons of physical buttons, and the combinations grow factorially — much faster than exponentially. It's very hard to find naming schemes that are both readable and minimal. I don't like Key Mapper's style of "trigger 1: (action 1), (action 2)," and when parameters aren't tuned well, commands can easily interfere with each other, making it unsuitable for general users. I'll consider giving it a shot in the Dev build in the future, but it likely won't be released in the public version.

</details>

</details>

---

<details>
<summary>Developer Recruitment and Contact</summary>

<br>

### Prerequisites

1. Thorough familiarity with Pro's features
2. Strict background screening
3. Programming development experience or programming logic skills

> I hope some professionals will join, because regarding API quota management, I'd like to move in a decentralized direction.

### Development Info

This app has gone through approximately **30 days** of development, **105 version updates**, and **tens of thousands** of detail corrections and tweaks. If you need version changelogs, historical source code, or APKs for research, please contact the author. If you encounter any bugs, find the interface unintuitive, or have any suggestions or questions about the app, you're also welcome to contact the author for discussion.

### Contact

📧 **Email:** fanpao757@gmail.com

> Please contact via email first. I will only provide private contact details if necessary or after you pass the Dev review.

</details>

</details>
