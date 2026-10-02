> **中文跟英文的語意是一樣的，只是作者英文比較不好（非母語使用者），所以先寫中文的介紹，用翻譯翻成英文後，依我想表達的語意微調用字，擇一閱讀即可，若有衝突，則以中文為準。**
>
> **阿我看不太懂各種授權是什麼意思，就隨便設了一個，我的想法是檔案開源，非營利可以隨便用，若要營利請私訊作者討論細節。**
> 
> **The Chinese and English versions convey the same meaning. The author is not a native English speaker, so the Chinese introduction was written first and then translated into English with minor wording adjustments to match the intended meaning. You only need to read one; if there are any conflicts, the Chinese version takes precedence.**
>
> **Oh, and I don't really understand what all the different licenses mean, so I just picked one at random. My intention is: the code is open-source, free for any non-commercial use; for commercial use, please DM the author to discuss the details.**

---

<details>
<summary><b>中文</b></summary>

<br>

<details>
<summary>程式起源與開發方式</summary>

<br>

用了很多款啟動器，都各有所長，但一直找不到完全符合我需求的，只好自己做一個。程式開發者是一個新手，程式能力不算太強，基本上都是提出構想之後叫AI寫，主要使用Arena AI aegent mode。

</details>

<details>
<summary>程式簡介</summary>

<br>

目前仍有許多地區在取得高性能運算裝置方面較為困難，作者也是從小使用中低階手機長大的，時常受到市面上遍地皆是的巨型臃腫程式荼毒，也持續有記憶體(ram)與儲存空間(rom)不夠用的問題，直到近幾年條件較好才有能力買較高階手機做開發，深諳性能不足之苦，所以一開始我只做我需要的功能，將省電、無動畫的快速載入與刷新、極低的性能需求與ram、rom佔用做為程式的主要設計語言，且儘量提供多一點兼容性，務讓極低階手機仍有一戰之力，延長其使用壽命。後來越做越多功能，說好聽是集各家所長，但好像快把我手機上所有不用聯網的功能都做上去了😂。

總之所以後來要公開的時候，就分出了功能極致精簡的Min跟全功能的Max，然後Max體積主要來自translate這個功能，所以如果想要Max的豐富功能，又想要極致輕量化的體積，沒有本地翻譯功能的Pro就應運而生，體積不到Max的1.2%(3)。

原本在安卓原生程式需要十數GB體積的功能，最後在我的濃縮下只要不到65MB(1)。另外，如果你不需要本地翻譯，不到800KB的Pro(2)功能多樣性與完整性絕對超乎你的想像，若你只想要極小體積，也用不太到Pro的各種複雜功能，則可以選擇Min，體積可再減超過一半(4)。如只需要部份Pro功能，又想要榨出每一分空間，可自行抓取原始碼做出各種功能排列組合的版本，若能力較弱，亦可誠心求取作者的幫助。(看情況幫，作者時間有限，希望不要太多請求)

(1)、(2) 經作者實測，Min、Pro、Max的apk體積分別是38KB、82KB、16.4MB，下載後未使用的rom佔用分別為135KB、271KB、17.6MB，Max下載本地translate包後，程式rom佔用為60.9MB(約43.2MB的包在我手機上被當快取)，用termux將本程式的dex2oat改成speed之後，程式rom佔用分別為367KB、767KB、64.9MB，正常使用情境(speed-profile)下應介於兩者之間，實際大小因實際使用情境與不同裝置版本而有差異，應以實際體驗為準

(3) 767/64900=0.01181818...

(4) 367/767=0.478487614...

</details>

<details>
<summary>這個程式對我來說的意義</summary>

<br>

這個程式大概取代了我手機的約15個app，每個app都是我精挑細選的，大概能覆蓋一般的5個程式，所以總體來說本程式大概等於市面上近百個普通的臃腫程式，原本這些app已經大幅提升了我的生產力與使用效率，只是功能太分散，有些也過於臃腫，在整合了之後，依我的邏輯精簡的互動，再搭配alias，更是讓我使用手機的效率大幅提升，只是不確定能不能賺回我用來開發的程式的時間就是了，但至少我在其中獲得了樂趣，有時也能確保我拿起手機卻打開了原本非預期開啟的程式。在公開之後，我也希望能幫助低性能安卓手機延長使用壽命，或是讓追求與眾不同的極客們多一點選擇與啟發(好像有點太有自信😂)。

</details>

<details>
<summary>指令列表與簡介</summary>

<br>

Pro與Max只列出相對Min與Pro的新增指令，相同功能不重複列出，完整指令亦可以在程式內使用「help」指令查詢，詳細功能以實際使用為準。

> <details>
> <summary>Min</summary>
> 
> <br>
> 
> ```
> alias - list all aliases or alias <name> <command> to set alias (use ; to set multiple)
> alias <name> - view one alias
> <app name> - launch an app (use exact name)
> apps - list installed apps
> help - show this list
> rm <alias name|toptext> - delete item
> status - show date time battery device ram rom temp bright vol wifi data bluetooth gps flash version, enter an item name to check its individual status (view only)
> color (above|below|background) - 可使用Hex色碼修改上方、下方、背景顏色，預設#FFFFFF|#00FF00|#000000
> fontsize - 可修改文字顯示大小，範圍為8-40間的正整數，預設18
> toptext <text|status item> - separate items with ;, wrapped/forced continuation lines start with |; use ;; to force a line break
> ```
> 
> </details>
> 
> <details>
> <summary>Pro</summary>
> 
> <br>
> 
> > <details>
> > <summary>help</summary>
> > 
> > <br>
> > 
> > ```
> > accessibility - list all accessibility features and explanations (enable "NPC's CLI Homescreen" in the system accessibility settings to use them)
> > AOD - show full screen clock or timer or stopwatch
> > BPM <non-negative integer> - start the metronome; BPM 0 stops it
> > calc <expression> - use calculator powered by exp4j library
> > calcs - show calculation history
> > compass - show the current heading (degrees, 16-point direction)
> > <date> - show that day's weekday(15821015-99991231) and lunar date (20260217-20560214)
> > flash - show the torch state; add [on|1|off|0|toggle|-1] to switch
> > gestures - show all gestures and their commands
> > jot <name> <content> - write a note
> > jotting <name> - view a note
> > jottings - list all notes and their contents
> > map|playstore|trans|yt <keyword> - search inside that app, web version as fallback
> > music - show playback, add [on|1|off|0|toggle|-1] to play local tracks (input prev or next to switch)
> > musics - list local audio files, then type a number to play
> > rec [on|1|off|0|toggle|-1] - record voice
> > recs - list recordings, then type a number to play
> > rm <item> - delete item (alias|calcs|gesture|history|jotting|toptext)
> > search <keyword> - search with the default engine (URL open directly)
> > settings - list all settings
> > status - show date time battery device ram rom temp bright vol wifi data bluetooth gps flash version(also can enter item name to check its individual status) ->亮度跟音量不是唯讀(read-only)了，其它可透過搭配自訂的alias與accessibility來達到調整的效果
> > ```
> > 
> > </details>
> > 
> > <details>
> > <summary>accessibility</summary>
> > 
> > <br>
> > 
> > ```
> > back - press the back button
> > home - press the home button
> > quicksettings - open the quick-settings panel
> > recents - open the recent apps overview
> > statusbar - expand the notification shade
> > trigger - listen for a pressed key and assign tap/2tap/hold commands to it
> > triggers - list every key and switch them all on or off
> > wait - pause that long before the next command (; separates the commands)
> > vibrate - Adding vibration to the script appropriately can serve as a reminder
> > x<number> y<number> - tap the screen at that point
> > ```
> > 
> > </details>
> > 
> > <details>
> > <summary>settings</summary>
> > 
> > <br>
> > 
> > ```
> > addtimems - status的time會加入三位毫秒(但好像不太準，參考就好，以實際體驗為準)，預設off
> > batterystyle - 電量顯示可選數字(num)或是四捨五入的方塊，有兩種方塊，一種是有總格數個方塊，實心方塊是剩餘電量，空心則是沒有的電量(mix)，另一種則是不顯示空心方塊(sol)，亦可自定總方塊數量
> > history - 以txt檔紀錄使用者輸入文字的歷史紀錄，預設off
> > holdtime 預設: 500ms max2tapgap 預設: 300ms
> > musicautooff <always|auto|none> (預設: auto) - 在設定的情況發生時，自動停止在本程式播放的本地音樂，防止社死的好東西(别問我為什麼會知道，或是為什麼要做這個功能) always = no connected Bluetooth audio device, auto = Bluetooth on-to-off, none = never
> > musicfolder、recfolder - 可設定本地音樂讀取的資料夾和錄音檔存放的資料夾
> > refreshspeed (time|compass|other) - 設定項目的刷新時間，預設1000ms|500ms|1s
> > swipepx 預設 105 tempunit 預設 °C
> > toptextshow (music|rec|bpm) - 在music、rec、bpm播放時顯示在toptext，預設都是on
> > 
> > AOD holdtime 預設500ms
> > AODcolor (number|background) 預設 #00FF00|#000000
> > AODmax2tapgap 預設300ms
> > TMFS (timerflash) 預設3
> > TMFSgap (timerflashgap) 預設0ms(代表閃爍總時間與振動時間一樣長，若不要閃爍請將TMFS設為0)
> > TMVB (timervibrate) 預設1000ms
> > ```
> > 
> > </details>
> 
> </details>
> 
> <details>
> <summary>Max</summary>
> 
> <br>
> 
> ```
> translate - power by Google ML Kit
> ```
> 
> </details>

</details>

<details>
<summary>權限需求</summary>

<br>

當然不同意也是可以的，只是需要權限的功能就無法使用。Pro跟Max一樣只列出相對Min、Pro多的部份。

> <details>
> <summary>Min</summary>
> 
> <br>
> 
> 偵測附近裝置 - 讀取wifi與藍牙狀態，但好像不同意也能偵測🤔
> 
> </details>
> 
> <details>
> <summary>Pro</summary>
> 
> <br>
> 
> 讀取裝置檔案 - music與rec功能使用，為了寫入與讀取的必要權限
> 
> 通知 - 可以錄音跟播放音訊的程式在新版安卓好像都需要通知，才能證明是使用者主動要做的，不是程式在背景亂搞
> 
> 麥克風 - 錄音就需要麥克風
> 
> 調整權限 - 可以調整裝置亮度跟音量
> 
> 震動 - 目前好像只有AOD的timer預設有震動，用到的地方不多，除非你在寫alias腳本時很常用到accessibility的vibrate
> 
> 無障礙 - 只有無障礙功能需要無障礙權限
> 
> </details>
> 
> <details>
> <summary>Max</summary>
> 
> <br>
> 
> 好像為了下載本地翻譯包有網路權限，但其它地方用不到
> 
> </details>

</details>

<details>
<summary>目前已知問題</summary>

<br>

1. 音量鍵設trigger之後，就算把動作改成調整音量，非處於播放音樂時，無法依靠音量鍵調整音量

</details>

<details>
<summary>不同安卓版本差異</summary>

<br>

1. 目前程式是寫短於1秒的錄音自動丟到垃圾桶，阿安卓11以下沒有內建垃圾桶，所以變成安卓11以下，短於1秒的錄音會直接被丟棄。
2. 安卓10以下無法寫入(編碼)opus格式的檔案，故安卓10以下只能使用效率較差的AMR-WB(3GP封裝)錄音，但一樣有使用VOICE_COMMUNICATION-能調用手機硬體的DSP(數位訊號處理器)做AEC(Acoustic Echo Cancellation，自適應回聲消除)、NS(Noise Suppression，噪音抑制)、AGC(Automatic Gain Control，自動增益控制)等三重降噪與提升人聲的演算法，安卓10以上則用ogg封裝的opus儲存錄音檔(recs)，兩者錄音只差在儲存效率上的不同，一樣都能錄音
3. 近幾代版本權限監管變嚴，很多功能都需要額外給權限才能使用或讀取，但基本上只要給滿權限都能使用，不會有差異

</details>

<details>
<summary>目前考慮過的功能</summary>

<br>

> <details>
> <summary>1. 多語言</summary>
> 
> <br>
> 
> 雖然作者是中文母語使用者，且英文超爛🤡，早期版本曾經想要做多語言，從英文、繁體中文、簡體中文開始，之後再看還有什麼需求，但後來功能越做越多，越做越複雜，有些指令翻成中文會變得挺複雜的，甚至有些我根本不知道怎麼翻💀，加上還要寫一堆映射指令，會大幅增加程式體積，也會降低運行效率，所以為了極致的效率，最後還是決定全英文，這個功能作者是不會更新的
> 
> </details>
> 
> <details>
> <summary>2. 修改jottings存放的位置</summary>
> 
> <br>
> 
> 就像musicfolder、recfolder一樣，作者曾經作過jottingsfolder，但不論我怎麼試，程式改了幾次，都讀不到這個程式的txt檔案，後來就放棄了，坐等大神指點迷津
> 
> </details>
> 
> <details>
> <summary>3. 簡單的離線遊戲</summary>
> 
> <br>
> 
> 像是貪食蛇、俄羅斯方塊之類的遊戲，在這個CLI界面可以很好的呈現，但作者不玩遊戲，做出來頂多玩一下就放著生灰了，遊戲內判斷的指令也不少，我有預感如果要統一設計語言，我會debug到崩潰，然後還是一樣有增加體積的問題，目前暫時不考慮更新
> 
> </details>
> 
> <details>
> <summary>4. 本地PDF檔案閱讀</summary>
> 
> <br>
> 
> 我曾使用我從2024年開始關注，程式製作當時剛發布 (2026 年 8 月 27 日發布)Android Jetpack PDF Viewer模組 (androidx.pdf)Beta版(1.0.0-beta01)，但不知為何debug了好幾個版本，不是當掉就是閃退，心態崩了，直接棄更這個功能，一樣求大神指路😭
> 
> </details>
> 
> <details>
> <summary>5. 更好的兼容性</summary>
> 
> <br>
> 
> > <details>
> > <summary>iOS</summary>
> > 
> > <br>
> > 
> > 因生態的隔閡，抱歉了 iPhone 用戶🥺，我曾經是有想讓你們可以用的，看未來生態能不能開放一點吧！如果有很多人想用，我也會嘗試做做看。
> > 
> > </details>
> > 
> > <details>
> > <summary>X86</summary>
> > 
> > <br>
> > 
> > 原本 AI 有給 v7a、v8a、x86、x86-64，但最後只保留了 v8a，因為：
> > 
> > ・電腦可用 Linux，其中有很多分支我覺得比我的程式更好用、更適合電腦，且是真正的 CLI（安卓看似表面是 CLI，但實際渲染邏輯仍是 GUI）
> > 
> > ・若覺得不好用，程度應該足以用 LFS（Linux From Scratch）自製
> > 
> > ・accessibility 只有安卓能用，鍵盤不確定能不能設 triggers（我沒有電腦）
> > 
> > ・為了極小體積
> > 
> > </details>
> > <summary>安卓</summary>
> > 
> > <br>
> > 
> > 近幾年連幾個比較開放的手機廠商都越來越難 root，目前市面上大多數安卓手機只能維持在原生系統，我覺得安卓手機在這方面有斷層與空洞。
> > 
> > 我的手機也是安卓 16，所以主要以此為基礎開發。從原本只支援安卓 16，到目前已拓展到 Min 支援安卓 5–17，Pro 與 Max 支援安卓 7–17。
> > 
> > </details>
> > 
> > <details>
> > <summary>鴻蒙</summary>
> > 
> > <br>
> > 
> > 我承認我沒有很了解這個系統的特性跟底層邏輯，所以目前有點難下指令開發，期待大佬的加入一起共創未來！
> > 
> > </details>
> 
> </details>
> 
> <details>
> <summary>6. 用API抓天氣跟雲端AI</summary>
> 
> <br>
> 
> 優點是在做到相同甚至更多、更好的功能的情況下，同時維持極小體積，缺點是需要網路，本來是想說做完全不需要網路的功能，但真的挺吸引人的，目前正以Pro為基礎的Dev(未公開)測試中，先嘗試了groq跟中央氣象署的API，還有什麼實用的API想推薦，或是想玩玩看Dev都可以私訊作者
> 
> </details>
> 
> <details>
> <summary>7. 取得ADB權限</summary>
> 
> <br>
> 
> 這個超讚，成功之後可以取代部份termux功能，trigger也能設定除了音量鍵以外的按鈕，但也是一樣做了好幾個版本之後一直沒有成功，如果需要這個功能的，我原本是用key mapper，推薦給你。雖然失敗了，但我還是覺得這個功能挺實用的，之後有空還是會考慮再嘗試看看，如果有大神願意幫忙，感激不盡
> 
> </details>
> 
> <details>
> <summary>8. triggers可以排列組合形成新指令</summary>
> 
> <br>
> 
> 目前問題是不好命名，目前音量鍵兩個，排列組合只要設兩種，但有些手機物理按鈕超多，排列組合是比指數快很多的階乘，兼具易讀性與極簡的命名很難找，不喜歡key mapper那種trigger 1：(動作1)、(動作2)的這種，而且參數調整不好時，指令間容易相互干擾，不適合一般人使用，未來會考慮在Dev做做看，但應該不會發布在公開版本
> 
> </details>

</details>

<details>
<summary>開發者招募與聯絡方式</summary>

<br>

想要加入開發者行列有幾個前提條件：(1)對Pro的功能瞭若指掌 (2)嚴格的背景審查 (3)具有程式開發經驗或具程式邏輯
希望能有一些專業人士加入，因為關於API的額度管理我想朝去中心化的方向製作

本程式經歷了約30天開發，105個版本更新，修正與微調了上萬個細節。若需要版本更新日誌或歷史版本的原始碼或apk做研究，請聯繫作者。如本程式出現了bug或界面不夠直覺的地方，或是對本程式有任何建議與疑問，也歡迎聯繫作者討論。

**作者的聯絡方式：**
Email：fanpao757@gmail.com
先用Email聯絡，如果有必要或是通過了Dev審核，我才會給私人聯絡方式

</details>

</details>

---

<details>
<summary><b>English</b></summary>

<br>

<details>
<summary>Origin and Development Approach</summary>

<br>

I've tried many launchers, each with its own strengths, but I could never find one that fully met my needs, so I decided to build my own. The developer is a beginner with modest programming skills; basically, I come up with ideas and have AI write the code, primarily using Arena AI agent mode.

</details>

<details>
<summary>Program Overview</summary>

<br>

There are still many regions where obtaining high-performance computing devices remains difficult. The author also grew up using low- to mid-range phones, constantly plagued by the bloated, oversized apps that are everywhere on the market, and perpetually struggling with insufficient memory (RAM) and storage (ROM). It wasn't until recent years, when my circumstances improved, that I could afford a higher-end phone for development. Having deeply experienced the pain of inadequate performance, I initially only built the features I needed, making power efficiency, animation-free fast loading and refreshing, and extremely low demands on performance, RAM, and ROM the core design principles of the app. I also tried to provide as much compatibility as possible, ensuring that even very low-end phones could still hold their own and extend their usable lifespan. Later, I kept adding more and more features — to put it nicely, I gathered the best of all worlds, but it feels like I've basically crammed every offline function from all the apps on my phone into this one 😂.

Anyway, when it came time to release it publicly, I split it into an ultra-minimalist Min and a full-featured Max. The bulk of Max's size comes from the translate feature, so for those who want the rich functionality of Max but also want an ultra-lightweight footprint, Pro — a Max without local translation — was born, with a size less than 1.2% of Max(3).

Features that would normally require over ten GB in a native Android app were condensed by me down to under 65 MB(1). Additionally, if you don't need local translation, Pro(2) at under 800 KB offers a diversity and completeness of features that will absolutely exceed your expectations. If you only want an extremely small footprint and don't really need the various complex features of Pro, you can choose Min, which reduces the size by more than half again(4). If you only need some of Pro's features and want to squeeze out every last byte of space, you can grab the source code and build your own variant with any combination of features. If your skills are limited, you're also welcome to sincerely ask the author for help. (Help is provided on a case-by-case basis; the author's time is limited, so please don't send too many requests.)

(1)(2) Based on the author's actual testing, the APK sizes of Min, Pro, and Max are 38 KB, 82 KB, and 16.4 MB respectively. After installation (unused), ROM usage is 135 KB, 271 KB, and 17.6 MB respectively. After Max downloads the local translate package, the app's ROM usage is 60.9 MB (the ~43.2 MB package is treated as cache on my phone). After using Termux to change this app's dex2oat mode to "speed," ROM usage becomes 367 KB, 767 KB, and 64.9 MB respectively. Under normal usage conditions (speed-profile), it should fall somewhere between these two extremes. Actual sizes vary depending on real usage scenarios and different device versions, so actual experience should be the reference.

(3) 767 / 64900 = 0.01181818...

(4) 367 / 767 = 0.478487614...

</details>

<details>
<summary>What This App Means to Me</summary>

<br>

This app has replaced roughly 15 apps on my phone, each of which I carefully hand-picked. Each of those apps could generally cover about 5 ordinary apps, so overall, this single app is roughly equivalent to nearly a hundred typical bloated apps on the market. Those original apps had already significantly boosted my productivity and efficiency, but their features were too scattered and some were overly bloated. After integrating them, streamlining the interactions according to my own logic, and pairing everything with aliases, my phone usage efficiency has improved dramatically. I'm just not sure if I'll ever recoup the time I spent developing it, but at least I had fun in the process, and sometimes it even ensures that when I pick up my phone, I don't accidentally open an app I didn't intend to. Now that it's public, I also hope it can help extend the lifespan of low-performance Android phones, or give geeks who seek something different a few more options and some inspiration (maybe a bit too confident of me 😂).

</details>

<details>
<summary>Command List and Brief Descriptions</summary>

<br>

For Pro and Max, only commands new relative to Min and Pro are listed; identical features are not repeated. The full command list can also be queried within the app using the "help" command. Detailed functionality is subject to actual use.

> <details>
> <summary>Min</summary>
> 
> <br>
> 
> ```
> alias - list all aliases or alias <name> <command> to set alias (use ; to set multiple)
> alias <name> - view one alias
> <app name> - launch an app (use exact name)
> apps - list installed apps
> help - show this list
> rm <alias name|toptext> - delete item
> status - show date time battery device ram rom temp bright vol wifi data bluetooth gps flash version, enter an item name to check its individual status (view only)
> color (above|below|background) - Use hex color codes to modify the top, bottom, and background colors. Defaults: #FFFFFF|#00FF00|#000000
> fontsize - Modify the text display size. Range: positive integers from 8 to 40. Default: 18
> toptext <text|status item> - separate items with ;, wrapped/forced continuation lines start with |; use ;; to force a line break
> ```
> 
> </details>
> 
> <details>
> <summary>Pro</summary>
> 
> <br>
> 
> > <details>
> > <summary>help</summary>
> > 
> > <br>
> > 
> > ```
> > accessibility - list all accessibility features and explanations (enable "NPC's CLI Homescreen" in the system accessibility settings to use them)
> > AOD - show full screen clock or timer or stopwatch
> > BPM <non-negative integer> - start the metronome; BPM 0 stops it
> > calc <expression> - use calculator powered by exp4j library
> > calcs - show calculation history
> > compass - show the current heading (degrees, 16-point direction)
> > <date> - show that day's weekday (15821015-99991231) and lunar date (20260217-20560214)
> > flash - show the torch state; add [on|1|off|0|toggle|-1] to switch
> > gestures - show all gestures and their commands
> > jot <name> <content> - write a note
> > jotting <name> - view a note
> > jottings - list all notes and their contents
> > map|playstore|trans|yt <keyword> - search inside that app, web version as fallback
> > music - show playback, add [on|1|off|0|toggle|-1] to play local tracks (input prev or next to switch)
> > musics - list local audio files, then type a number to play
> > rec [on|1|off|0|toggle|-1] - record voice
> > recs - list recordings, then type a number to play
> > rm <item> - delete item (alias|calcs|gesture|history|jotting|toptext)
> > search <keyword> - search with the default engine (URL open directly)
> > settings - list all settings
> > status - show date time battery device ram rom temp bright vol wifi data bluetooth gps flash version (also can enter item name to check its individual status) -> Brightness and volume are no longer read-only; other items can be adjusted by combining custom aliases with accessibility features.
> > ```
> > 
> > </details>
> > 
> > <details>
> > <summary>accessibility</summary>
> > 
> > <br>
> > 
> > ```
> > back - press the back button
> > home - press the home button
> > quicksettings - open the quick-settings panel
> > recents - open the recent apps overview
> > statusbar - expand the notification shade
> > trigger - listen for a pressed key and assign tap/2tap/hold commands to it
> > triggers - list every key and switch them all on or off
> > wait - pause that long before the next command (; separates the commands)
> > vibrate - Adding vibration to the script appropriately can serve as a reminder
> > x<number> y<number> - tap the screen at that point
> > ```
> > 
> > </details>
> > 
> > <details>
> > <summary>settings</summary>
> > 
> > <br>
> > 
> > ```
> > addtimems - The time in status will include three-digit milliseconds (though it doesn't seem very accurate, so take it as a rough reference; actual experience may vary). Default: off
> > batterystyle - Battery display can be numeric (num) or rounded blocks. There are two block styles: one shows the total number of blocks, with filled blocks representing remaining battery and hollow blocks representing depleted battery (mix); the other hides the hollow blocks entirely (sol). The total number of blocks can also be customized.
> > history - Records the user's input history in a txt file. Default: off
> > holdtime Default: 500ms  max2tapgap Default: 300ms
> > musicautooff <always|auto|none> (Default: auto) - Automatically stops locally played music within this app when the specified condition occurs — a great feature for preventing social embarrassment (don't ask me how I know, or why I built this feature). always = no connected Bluetooth audio device, auto = Bluetooth on-to-off, none = never
> > musicfolder, recfolder - You can set the folder for reading local music and the folder for storing recordings.
> > refreshspeed (time|compass|other) - Set the refresh interval for items. Defaults: 1000ms|500ms|1s
> > swipepx Default: 105  tempunit Default: °C
> > toptextshow (music|rec|bpm) - Display in toptext when music, rec, or bpm is playing. All default to on.
> > 
> > AOD holdtime Default: 500ms
> > AODcolor (number|background) Default: #00FF00|#000000
> > AODmax2tapgap Default: 300ms
> > TMFS (timerflash) Default: 3
> > TMFSgap (timerflashgap) Default: 0ms (meaning the total flash duration equals the vibration duration; set TMFS to 0 if you don't want flashing)
> > TMVB (timervibrate) Default: 1000ms
> > ```
> > 
> > </details>
> 
> </details>
> 
> <details>
> <summary>Max</summary>
> 
> <br>
> 
> ```
> translate - powered by Google ML Kit
> ```
> 
> </details>

</details>

<details>
<summary>Permission Requirements</summary>

<br>

Of course, you can decline them, but features that require those permissions won't be available. Pro and Max only list permissions beyond those of Min and Pro, respectively.

> <details>
> <summary>Min</summary>
> 
> <br>
> 
> Detect nearby devices — reads Wi-Fi and Bluetooth status, though it seems like detection still works even if you decline 🤔
> 
> </details>
> 
> <details>
> <summary>Pro</summary>
> 
> <br>
> 
> Read device files — used by the music and rec features; a necessary permission for reading and writing.
> 
> Notifications — apps that can record and play audio seem to require notification permission on newer Android versions to prove the user initiated the action and the app isn't doing things in the background.
> 
> Microphone — recording requires the microphone.
> 
> Adjust settings — allows adjusting device brightness and volume.
> 
> Vibration — currently only the AOD timer has vibration enabled by default; not used in many places unless you frequently use the accessibility vibrate command in your alias scripts.
> 
> Accessibility — only accessibility features require the accessibility permission.
> 
> </details>
> 
> <details>
> <summary>Max</summary>
> 
> <br>
> 
> It seems network permission is needed for downloading the local translation package, but it's not used anywhere else.
> 
> </details>

</details>

<details>
<summary>Currently Known Issues</summary>

<br>

1. After setting a volume key as a trigger, even if the action is changed to adjust volume, the volume keys cannot adjust the volume when music is not playing.

</details>

<details>
<summary>Differences Across Android Versions</summary>

<br>

1. Currently, the app automatically discards recordings shorter than 1 second to the trash. However, Android 11 and below don't have a built-in trash bin, so on Android 11 and below, recordings shorter than 1 second are permanently deleted.
2. Android 10 and below cannot write (encode) Opus-format files, so on Android 10 and below, only the less efficient AMR-WB (3GP container) can be used for recording. However, it still uses VOICE_COMMUNICATION mode, which can leverage the phone's hardware DSP (Digital Signal Processor) for AEC (Acoustic Echo Cancellation), NS (Noise Suppression), and AGC (Automatic Gain Control) — a triple noise-reduction and voice-enhancement algorithm. Android 10 and above use Ogg-container Opus for storing recordings (recs). The only difference between the two is storage efficiency; both can record just fine.
3. In recent Android versions, permission controls have become stricter, and many features require additional permissions to use or access. However, as long as you grant all permissions, everything should work without differences.

</details>

<details>
<summary>Features I've Considered</summary>

<br>

> <details>
> <summary>1. Multi-language support</summary>
> 
> <br>
> 
> Although the author is a native Chinese speaker with terrible English 🤡, early versions once aimed to support multiple languages, starting with English, Traditional Chinese, and Simplified Chinese, then expanding based on demand. However, as features grew more numerous and complex, some commands became quite complicated to translate into Chinese, and some I honestly have no idea how to translate 💀. On top of that, writing a bunch of mapped commands would significantly increase the app size and reduce runtime efficiency. So, in the pursuit of ultimate efficiency, I ultimately decided to keep everything in English. The author will not be updating this feature.
> 
> </details>
> 
> <details>
> <summary>2. Changing the jottings storage location</summary>
> 
> <br>
> 
> Just like musicfolder and recfolder, the author once implemented a jottingsfolder, but no matter how I tried or how many times I rewrote the code, the app couldn't read its own txt files from that location. I eventually gave up and am waiting for an expert to point me in the right direction.
> 
> </details>
> 
> <details>
> <summary>3. Simple offline games</summary>
> 
> <br>
> 
> Games like Snake or Tetris could be nicely rendered in this CLI interface. However, the author doesn't play games, so at best I'd play for a bit and then let it gather dust. The in-game logic commands are also quite numerous, and I have a feeling that if I tried to unify the design language, I'd debug myself into a breakdown. Plus, there's the same issue of increased app size. Not considering this for now.
> 
> </details>
> 
> <details>
> <summary>4. Local PDF file reading</summary>
> 
> <br>
> 
> I tried using the Android Jetpack PDF Viewer module (androidx.pdf) Beta (1.0.0-beta01), which I had been following since 2024 and which was just released (August 27, 2026) around the time I was building the app. But for some reason, after debugging through several versions, it either froze or crashed. I lost my sanity and abandoned this feature entirely. Once again, begging for an expert's guidance 😭
> 
> </details>
> 
> <details>
> <summary>5. Better compatibility</summary>
> 
> <br>
> 
> > <details>
> > <summary>iOS</summary>
> > 
> > <br>
> > 
> > Due to the ecosystem barrier, sorry iPhone users 🥺. I did once want to make this available to you — let's see if the ecosystem opens up a bit in the future! If enough people want it, I'll also try to give it a shot.
> > 
> > </details>
> > 
> > <details>
> > <summary>x86</summary>
> > 
> > <br>
> > 
> > Originally, the AI gave me builds for v7a, v8a, x86, and x86-64, but in the end I kept only v8a, because:
> > 
> > ・Computers can run Linux, and I think many of its distributions are better and more suitable for computers than my app, and they are true CLI (on Android, the surface looks like CLI, but the actual rendering logic still runs on GUI)
> > ・If those still don't satisfy you, your skill level should be enough to build your own with LFS (Linux From Scratch)
> > ・accessibility only works on Android, and I'm not sure if keyboards can be set as triggers (I don't own a computer)
> > ・For an ultra-small footprint
> > 
> > </details>
> > 
> > <details>
> > <summary>Android</summary>
> > 
> > <br>
> > 
> > In recent years, even the more open phone manufacturers have made rooting increasingly difficult. Most Android phones on the market can only stay on stock systems, and I feel there's currently a product gap and void in this area for Android phones.
> > 
> > My phone also runs Android 16, so I developed primarily based on it. Starting from supporting only Android 16, the app has now expanded to support Android 5–17 for Min, and Android 7–17 for Pro and Max.
> > 
> > </details>
> > 
> > <details>
> > <summary>HarmonyOS</summary>
> > 
> > <br>
> > 
> > I admit I don't really understand the characteristics and underlying logic of this system, so it's currently hard for me to develop for it. Looking forward to experts joining in to create the future together!
> > 
> > </details>
> 
> </details>
> 
> <details>
> <summary>6. Using APIs for weather and cloud AI</summary>
> 
> <br>
> 
> The advantage is achieving the same or even more and better features while maintaining an ultra-small footprint. The downside is that it requires an internet connection. I originally intended to build a completely offline app, but this is really quite appealing. Currently being tested in a Dev (unreleased) build based on Pro. I've tried the Groq and Central Weather Administration APIs so far. If you have any useful APIs to recommend or want to try out Dev, feel free to DM the author.
> 
> </details>
> 
> <details>
> <summary>7. Obtaining ADB permissions</summary>
> 
> <br>
> 
> This one is amazing — if successful, it could replace part of Termux's functionality, and triggers could be set for buttons other than the volume keys. But similarly, after several iterations, I never got it working. If you need this feature, I originally used Key Mapper — recommended. Although I failed, I still think this feature is quite practical, so I might try again when I have time. If any experts are willing to help, I'd be extremely grateful.
> 
> </details>
> 
> <details>
> <summary>8. Combining triggers to form new commands</summary>
> 
> <br>
> 
> The current problem is that they're hard to name. With just two volume keys, only two combinations need to be defined, but some phones have tons of physical buttons, and the combinations grow factorially — much faster than exponentially. It's very hard to find naming schemes that are both readable and minimal. I don't like Key Mapper's style of "trigger 1: (action 1), (action 2)," and when parameters aren't tuned well, commands can easily interfere with each other, making it unsuitable for general users. I'll consider giving it a shot in the Dev build in the future, but it likely won't be released in the public version.
> 
> </details>

</details>

<details>
<summary>Developer Recruitment and Contact</summary>

<br>

**Prerequisites for joining the development team:** (1) Thorough familiarity with Pro's features (2) Strict background screening (3) Programming development experience or programming logic skills.
I hope some professionals will join, because regarding API quota management, I'd like to move in a decentralized direction.

This app has gone through approximately 30 days of development, 105 version updates, and tens of thousands of detail corrections and tweaks. If you need version changelogs, historical source code, or APKs for research, please contact the author. If you encounter any bugs, find the interface unintuitive, or have any suggestions or questions about the app, you're also welcome to contact the author for discussion.

**Author's Contact Information:**
Email: fanpao757@gmail.com
Please contact via email first. I will only provide private contact details if necessary or after you pass the Dev review.

</details>

</details>
