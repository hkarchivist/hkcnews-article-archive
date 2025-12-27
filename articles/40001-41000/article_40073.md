---
title: "唔想俾黑客偷睇你約妹豬食飯 　End to End Encryption或者幫到你"
date: "2021-04-08"
last_updated: "2021-04-09 13:09:13"
author: "專業和你傾"
category: "眾說"
tags:
  - "資訊科技界"
  - "資訊安全"
  - "點對點加密"
url: "https://web.archive.org/web/20210408060249/https://www.hkcnews.com/article/40073/%E8%B3%87%E8%A8%8A%E5%AE%89%E5%85%A8-%E9%BB%9E%E5%B0%8D%E9%BB%9E%E5%8A%A0%E5%AF%86-%E8%B3%87%E8%A8%8A%E7%A7%91%E6%8A%80%E7%95%8C-40073/%E5%94%94%E6%83%B3%E4%BF%BE%E9%BB%91%E5%AE%A2%E5%81%B7%E7%9D%87%E4%BD%A0%E7%B4%84%E5%A6%B9%E8%B1%AC%E9%A3%9F%E9%A3%AF-end-to-end-encryption%E6%88%96%E8%80%85%E5%B9%AB%E5%88%B0%E4%BD%A0"
original_url: "https://www.hkcnews.com/article/40073/%E8%B3%87%E8%A8%8A%E5%AE%89%E5%85%A8-%E9%BB%9E%E5%B0%8D%E9%BB%9E%E5%8A%A0%E5%AF%86-%E8%B3%87%E8%A8%8A%E7%A7%91%E6%8A%80%E7%95%8C-40073/%E5%94%94%E6%83%B3%E4%BF%BE%E9%BB%91%E5%AE%A2%E5%81%B7%E7%9D%87%E4%BD%A0%E7%B4%84%E5%A6%B9%E8%B1%AC%E9%A3%9F%E9%A3%AF-end-to-end-encryption%E6%88%96%E8%80%85%E5%B9%AB%E5%88%B0%E4%BD%A0"
---

# 唔想俾黑客偷睇你約妹豬食飯 　End to End Encryption或者幫到你

<figure>
<img src="https://web.archive.org/web/20210412060643im_/https://hkcnews.com/news_新聞/hk-discuss/2021/04/資訊科技界-專業和你傾-資料外洩-20210408114506_556b_large.png" alt="">
</figure>

【撰文：資訊科技界選委黃浩華】

Instant Messenger已經成為我哋同朋友溝通常用嘅工具，但係最近幾年資安事故頻密發生，要確保通訊無咁易俾壞人知道，除咗set好個password同用Multi-Factor Authentication（MFA）之外，用軟件時應該留意下軟件有無點對點加密功能。

講點對點加密之前，先理解下到底平時啲電腦係點樣做加密嘅呢？ **電腦加密一般嚟講可以分兩類，對稱式加密（Symmetric Encryption）同非對稱式加密（Assymetric Encryption）。關鍵分別在於加密同解密用嘅鎖匙到底係咪同一條，一個得一條鎖匙另一個就有兩條唔一樣嘅鎖匙** ，前者就會用同一條鎖匙完成加密同解密嘅程序，即係平時喺 Zip File 或者 Excel加密碼一樣，只要用返同一個密碼就可以解密個檔案。後者呢就唔同啦，兩條鎖匙內容唔同，一條鎖匙（Public Key）係可以公開，另一條鎖匙（Private Key）就唔可以公開，一定要收埋好佢。公開嗰條係專用嚟俾其他人去加密內容，並唔包括解密功能，自己收埋嗰條就專用嚟解密返加密咗嘅內容。

<figure>
<img src="https://web.archive.org/web/20210412060643im_/https://hkcnews.com/news_新聞/hk-discuss/2021/04/電腦加密-資訊安全-encryption-20210407185757_2b27_large.png" alt="">
<figcaption>Open PGP Encryption, 插圖來源：goanywhere.com</figcaption>
</figure>

### 公開鎖匙只有加密功能

非對稱式加密看似繁複，但係好處就係可以將加密同解密步驟分開，喺確保第三方加密者係唔需要知道解密方法都可以加密訊息，因為公開鎖匙只有加密功能嘅關係，公開嘅 Public Key 就算俾唔熟悉嘅人知道，仍然唔會令到你嘅訊息洩漏。其實日常生活中大家用嘅 email 或者網站好多時（唔係所有，例如你上 Google Chrome 時無鎖嘅網站就要小心）已經用咗非對稱式加密，上網時一般用戶用 Public Key，而服務供應商持有 Private Key，確保訊息只有你同服務供應商先知道。

不過今時今日服務供應商唔一定係信得過嘅一方，服務供應商可能請咗啲會偷睇用戶訊息嘅工程師，或者因壓力將原始資料交俾第三方。點對點加密就係為咗咁嘅情況誕生，一般而言，如果妹豬係收訊息一方，真正持有 Private Key 就只有妹豬嘅電話，而我就持有妹豬嘅 Public Key，服務供應商係唔會有任何 Private Key。喺約妹豬食飯過程中，我會用妹豬嘅 Public Key 加密內容，服務供應商亦只會收到加密咗嘅內容，而當妹豬收到加密內容後，程式就會用妹豬手機內嘅 Private Key 解密訊息，咁就可以安全約食飯啦。

### 使用軟件要保持警覺

**點對點加密本身設計上無問題，唔代表用起上嚟就一定安全，例如 WhatsAapp 喺 2017年就俾人發現有漏洞，公司可以攔截用戶訊息，又例如 protonmail 有點對點加密，但只限於兩者都用 protonmail 通訊嘅情況，protonmail send 去 gmail都係無點對點加密。** 所以就算軟件聲稱有點對點加密，都要睇清楚實際上係點。大家用軟件時要無時無刻保持警覺，咁中伏嘅機會先會大減。

**作者簡介：** 黃浩華，數據科學家、資訊科技界選委、2020年立法會資訊科技界參選人。主力推動開放數據，網絡自由，資訊保安，本地創科。


---


請加入成為眾新聞的月費訂戶，長期支持我們的工作。所有訂戶都可以收到我們的「每周時事」通訊 。

月費訂戶 [網址：hkcnews.com/aboutus/#subscribe](/web/20210412060643/https://hkcnews.com/aboutus/#subscribe)

---

![博客 | 專業和你傾](https://web.archive.org/web/20210412060643im_/https://hkcnews.com/uploads/avatars/88429582-e9f9-4fb6-aa3a-a559ac157714.png?1364096645)

**博客 | 專業和你傾**

【專業和你傾】十二個專業團體輪流執筆
