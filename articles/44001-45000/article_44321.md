---
title: "如何較安全地使用雲端檔案儲存空間"
date: "2021-08-12"
author: "Pazu薯伯伯"
category: "眾說"
tags:
  - "薯伯伯"
  - "雲端"
url: "https://web.archive.org/web/20211027133108/https://hkcnews.com/article/44321/%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD-%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD-44321/%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD"
original_url: "https://hkcnews.com/article/44321/%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD-%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD-44321/%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD%EF%BF%BD"
---

# 如何較安全地使用雲端檔案儲存空間

<figure>
<img src="https://web.archive.org/web/20211027133108im_/https://hkcnews.com/news_新聞/hk-discuss/2021/08/雲圖-雲端-薯伯伯-20210812164251_19ca_large.jpg" alt="">
</figure>

儲存檔案在雲端甚為方便，但用得不妥當，隨時方便自己，亦方便歹徒，所以使用雲端服務時，更應加倍小心。

有三點要注意：

一，基本保安要求，密碼、二步認證

二，雲端儲存空間上較敏感的資料應額外加密

三，慎選雲端服務供應商

以下逐點去講。

不論你用哪間服務供應商，但基本的保安必須做好，包括密碼不重複，不會與其他戶口共用密碼，並且要有開啟二步認證。若然密碼太多記不住，就要習慣使用密碼管理器。如果密碼重複使用，萬一另一間網絡供應商的資料外洩了（經常發生），別人就能猜到你其他戶口的密碼。

有關密碼管理器： [https://www.patreon.com/posts/38002570](https://web.archive.org/web/20211027133108/https://www.patreon.com/posts/38002570)

二步認證的設置： [https://www.patreon.com/posts/38002570](https://web.archive.org/web/20211027133108/https://www.patreon.com/posts/38002570)

檔案放上雲端，要作好最壞打算，隨時有被盜的風險，不要心存僥倖。入侵的方式可以是外部，但也有可能是該公司出賣客戶資料。對於較為敏感的檔案，當然最好避免上傳至雲端，但若然自己衡量風險後認為要放上雲端，就建議要做一層額外的加密。

有兩種加密方式，分別是在本機電腦用Veracrypt製作加密碟，或使用附加在Google Drive或Dropbox的加密服務。

甲，在本機電腦用Veracrypt製作加密碟

Veracrypt的使用方法大致是，在電腦上使用免費開源的Veracrypt軟件，製造一個加密碟影像檔案，使用起來好像是一個虛擬的USB手指，實質只是一個檔案。

在電腦上打開Veracrypt，選擇加密碟影像檔案，把檔案放入去，之後再把整個加密碟影像檔案上傳至雲端。由於每次一有微細的檔案更改，都要整個加密碟檔案重新上傳，所以加密碼碟不宜太大。

好處：Veracrypt是資訊保安界裡其中一個最廣為使用的加密工具，運作非常穩定。

壞處：只能在Mac、PC等電腦上操作，檔案不能在手機上解鎖。另外，對新手來說，操作上有點複雜。

我之前寫過一篇文章介紹Veracrypt，請看： [https://www.patreon.com/posts/38341752](https://web.archive.org/web/20211027133108/https://www.patreon.com/posts/38341752)

乙，附加在Google Drive或Dropbox的加密服務

Google Drive、Dropbox、OneDrive等最流行的服務，都不是「零知識」，即是他們有能力把你的資料向他們披露。他們會不會這樣做是一回事，但我就是不喜歡他們有這個權限。

其中一個簡單的解決方法，是使用 [Cryptomator](https://web.archive.org/web/20211027133108/https://cryptomator.org/downloads/) ，能夠在Google Drive、Dropbox、OneDrive上加入一個加密文件夾，放進去的資料，即使是總公司，也不能查看當中內容。

電腦版免費使用，但手機app要付費。

好處：手機及電腦均能解密，方便使用。

壞處：在網上論壇，經常有人提及自己以Cryptomator（或另一類似軟件Boxcryptor），會有些檔案消失，可能是使用者使用不當，也有可能是其他原因，而更重要是，我自己有次也出現過類似情況。所以，即使用這個軟件，我也只會加密非常少量檔案，而絕不敢用它來加密整個Google Drive。另外，檔案本身也有較好的備份。

三，慎選雲端服務供應商：推介 [Tresorit](https://web.archive.org/web/20211027133108/https://tresorit.com/individuals)

雲端檔案儲存系統，最流行的是Google Drive、Dropbox、Onedrive等，但這些都不是「零知識」，即是這些服務的公司理論上都能查看用戶的資料。公平一點說，不是任何一個員工都有此權限，而看過檔案的員工也會留有記錄，如果是法庭要求交出資料，美國的科技巨頭也會在其《透明報告》中披露相關數據。

但問題是，我為甚麼要任由別人去決定如何保管我的資料？我不管他們會否交出我的檔案，但我對於他們這個能力，已覺不舒服。所以我寧願多付一點錢，選擇一間對我的檔案是「零知識」的服務商，即是檔案有加密，而服務供應商沒有密鑰，亦無法打開我的任何檔案。

考慮到公司背景、所在國瑞士、審計報告、風評、用戶組織等等，我推介的是Tresorit。該公司設在瑞士及匈牙利，要遵照瑞士及歐盟的私隱政策，數據中心設在愛爾蘭及荷蘭。Tresorit 在2021被瑞士郵政收購，雖然郵政也是政府機關，但一來該公司利用「零知識」的運作模式，想出賣用戶數據也沒有甚麼可以出賣，二來該政府是瑞士，出名對私隱保護較強，不像某些下流的國度。

Tresorit的功能與Google Drive類似，都是雲端硬盤，但是「零知識」，他們沒有能力查看用戶檔案。使用起來也大同小異，但涉及大量人工智能搜索功能就欠奉，這點算是一個妥協。另外，Tresorit本身都有加密，所以不用搭配Cryptomator。

網址： [https://tresorit.com/individuals](https://web.archive.org/web/20211027133108/https://tresorit.com/individuals)

申請時會有十四天免費試用期，在十四天內取消，計劃會變成Basic，基本的計劃應該也有Camera Upload（相簿同步）的功能。Tresorit的價錢稍貴，Premium計劃每月10.42美金（500 GB空間），Solo計劃每月24美金（2500 GB空間）。

如果有學校edu尾（包含edu.hk）的電郵地址，可以直接發信給Support查詢並取得八折優惠。如果是注冊的非牟利組織，更有5折優惠。學生優惠要聯絡 [[email protected]](/web/20211027133108/https://hkcnews.com/cdn-cgi/l/email-protection) 。非牟利組織的優惠則要看 [https://tresorit.com/subscribe-nonprofit](https://web.archive.org/web/20211027133108/https://tresorit.com/subscribe-nonprofit) 。

另有幾間點對點加密的雲端硬盤，例如加拿大的Sync.com，以及pCloud、CrashPlan（慢慢慢）、SpiderOak，我自己測試過，覺得速度未如理想，而Proton Drive暫時仍屬beta版，空間不大。Tresorit及Sync.com均有試用期，不妨試一星期才決定用哪個。至於NAS，我不是太確定其安全系數，沒有使用。

Tresorit好處：速度算快，手機及電腦的應用介面易用，運作方式是「零知識」，即該公司沒有能力出賣你。注冊國在瑞士，對私隱保障佳。

Tresorit壞處：較錢會是其中一個最大的阻力，其實也不是太貴，但因為Google Drive太便宜，大多數人會以此為價格的參考基準。

整體而言我對Tresorit很滿意。

總結：

最敏感的檔案不只不應上傳至雲端，甚至不應該儲存在可以上網的設備，有些人甚至會刻意把專門儲存敏感資料的電腦的上網元件拆除，確保完全與網絡隔絕，即所謂的「氣隙」（air gap）。

但如果真的要把檔案放到雲端，較理想的做法是選用Tresorit這些零知識的雲端檔案儲存空間。如果不能負擔，使用Google Drive等，則應把較敏感的資料以Veracrypt或Cryptomator加密。

較理想的雲端方案：Tresorit

次理想的雲端方案：Google Drive / Dropbox + Veracrypt

或：Google Drive / Dropbox + Cryptomator（只加密少量檔案）

另外有一點想提，一些服務供應商可以透過改變註冊地來改變儲存雲端檔案的地理位置，例如由人權較差的國家轉至人權較好的國家，但一來政策不是太透明，二來不是所有服務都有提供相關選項（Google似乎要商業用戶才有此選項）。如果改到就改，最好還是選用更安全可靠的服務商。

圖：很久沒有從飛機上看過雲，放一張雲圖來應景。我想起多年前有位 [印度稅務局前官員 Vishwa Bandh](https://web.archive.org/web/20211027133108/https://youtu.be/AnxrJiS5uKU?t=133) 曾經說過，雲端的軟件（CD？）及檔案很危險，但無人預料得到，萬一打風落雨怎麼辦。

🔑 [【超務實長清單整理，和你加強資訊保安、私隱保護（2021年8月更新）】](https://web.archive.org/web/20211027133108/https://www.patreon.com/posts/54385202)

原文刊於 [作者Patreon](https://web.archive.org/web/20211027133108/https://www.patreon.com/posts/54741568)


---


請加入成為眾新聞的月費訂戶，長期支持我們的工作。所有訂戶都可以收到我們的「每周時事」通訊 。

月費訂戶 [網址：hkcnews.com/aboutus/#subscribe](/web/20211027133108/https://hkcnews.com/aboutus/#subscribe)

---

![博客 | Pazu薯伯伯](https://web.archive.org/web/20211027133108im_/https://hkcnews.com/uploads/avatars/001d8f85-a098-4d95-b480-83af95b083b9.png?562121451)

**博客 | Pazu薯伯伯**

【Pazu薯伯伯・旅遊寫作人】薯伯伯為最早一批在網上連載遊記的香港人，多年來足迹遍佈歐、亞多國，在喜馬拉雅山麓、東南亞、南亞等地區生活。著有《風轉西藏》、《北韓迷宮》、《西藏西人西事》及《不正常旅行研究所》，分別在香港、北京及首爾出版。
作者 Facebook：https://www.fb.com/pazukong；
Patreon 頻道：https://www.patreon.com/pazu
