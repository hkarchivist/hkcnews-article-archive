---
title: "PopVote安全問題未解決　再發現新問題"
date: "2017-02-12"
author: "讀者來論"
category: "眾說"
tags:
  - "特首民投"
  - "popvote"
url: "https://web.archive.org/web/20210704083525/https://www.hkcnews.com/article/1715/popvote%E5%AE%89%E5%85%A8%E5%95%8F%E9%A1%8C%E6%9C%AA%E8%A7%A3%E6%B1%BA-%E5%86%8D%E7%99%BC%E7%8F%BE%E6%96%B0%E5%95%8F%E9%A1%8C"
original_url: "https://www.hkcnews.com/article/1715/popvote%E5%AE%89%E5%85%A8%E5%95%8F%E9%A1%8C%E6%9C%AA%E8%A7%A3%E6%B1%BA-%E5%86%8D%E7%99%BC%E7%8F%BE%E6%96%B0%E5%95%8F%E9%A1%8C"
---

# PopVote安全問題未解決　再發現新問題

<figure>
<img src="https://web.archive.org/web/20210704083525im_/https://www.hkcnews.com/news_新聞/hk-discuss/2017/02/特首民投-popvote-特首選戰-20170212201633_22d8_large.png" alt="">
<figcaption>截至今晚8時許，PopVote上面前三名參選人的得票數。</figcaption>
</figure>

除了早前被發現的嚴重的保安問題和資料外洩風險 [[1]](https://web.archive.org/web/20210704083525/https://www.hkcert.org/my_url/zh/blog/17020901) 外， [前線科技人員](https://web.archive.org/web/20210704083525/https://www.facebook.com/FrontlineTechWorkersConcernGroup/?fref=ts) 的團隊經過調查，昨日再發現 PopVote 系統存在其他的保安和設計漏洞，已即時通知 PopVote 普及投票及負責系統技術的 Civic Data 公民數據的負責人，該漏洞增加資料外洩的機會和影響投票可信性。

## 登入憑證外洩風險

PopVote 把用戶的 Telegram 登入憑證（Session Authentication Key）存放在瀏覽器的本地儲存（localStorage）內，即使關閉瀏覽器或重新啓動電腦，該登入憑證不會被清除而且繼續有效。該瀏覽器的任何使用者，例如公共圖書館或學校的公用電腦的其他用戶，可以取得這個憑證，登入該用戶的 Telegram 戶口，存取該用戶的所有通話記錄及收發新訊息。

該系統在2月8日的更新中修正了投票程序完成後未有登出 Telegram 的問題。這個修正本應能減低上述漏洞的影響，可是我們發現這個修正未有妥善處理用戶未完成投票程序時的情況。如果用戶沒有完成投票程序，就算關閉瀏覽器，重開後仍然保持登入。故此，用戶仍然可以因為這個漏洞而被竊取Telegram戶口。

## 投票結果可信性

在 2012 和 2014 年的民間投票當中，系統要求用戶以香港網絡登入，並且使用本地電話號碼透過短訊（SMS）確認。這個設計的原意是確保只有香港居民才能參與投票，並且增加種票的成本。

然而，新的 PopVote 系統改為以 Telegram 登入後，取消了只限本地網絡的規定。雖然系統要求用戶填寫本地電話號碼登入 Telegram，我們卻發現 PopVote 存在明顯的設計漏洞，以致未能有效防止其他國家的電話登入投票。利用這個漏洞，前線科技人員成功在海外以外國電話投票。   
 這個漏洞令種票成本下降，減低投票結果的可信性。

## 電話和身份證號碼外洩風險

PopVote 在他們的聲明 [2] 和 Q&A [3] 中聲稱用戶的身分證和電話號碼會在客戶端「產生散列（hash value）」，用戶的個人資料「絕不會直接傳給 PopVote 後台系統」，「不論是 PopVote 系統還是駭客，都極難還原成有用的資料」。

我們的團隊發現，該系統在客戶端所用的散列算法（hash function）是單純的 SHA256。SHA256 本身是安全的，可是 PopVote 在使用該算法時未有留意輸入的資料本身的組合有限。我們的實驗顯示，根本無需破解散列算法，只需十分鐘就能製作所有香港身分證和電話號碼「散列」的對照表。任何人（包括 PopVote）只須持有該對照表，便能即時解讀任何「散列」所代表的個人資料。

這個問題本身並非安全漏洞，可是從 PopVote 的系統設計，以至團隊的對外宣傳當中，顯示出團隊對加密算法的特性以及資訊安全缺乏認知，使我們對 PopVote 團隊是否有能力合理地保障用戶的敏感訊息抱有疑問。

> 建議   
>  基於之前所發現的嚴重保安漏洞仍未修正，我們維持之前的建議，呼籲市民立即停用該系統。   
>  任何曾經使用該系統的市民，應了解基於之前發現的嚴重保安漏洞而引致的通訊紀錄外洩風險，並採取適當措施保護各下的資訊安全 [1]。   
>  對於所有依賴 PopVote 普及投票結果或對結果進行分析的市民，請留意雖然該系統要求用戶填寫本地電話號碼和通過短訊確認，該系統並未能保證投票人持有或控制一個本地電話號碼，投票結果的可信性可能受影響。

對於 PopVote 普及投票，我們認為對方未有妥善考慮公眾安全，而且對結果的可信性有疑問。前線科技人員團隊、曾參與 2012 和 2014 民間投票系統設計和審核的工程師、資訊安全專家等，於系統開放的第一天起已經和他們進行多場會議，指出問題並提出協助。然而，PopVote 團隊及其負責人不但未有認真回應各項安全和設計上的漏洞，反而不斷接受傳媒訪問，以技術語言隱瞞問題，讓大眾誤以為漏洞已處理。我們對 PopVote 團隊及其負責人處理用戶安全的輕率態度感到失望。

盡責披露

我們已在發佈上述漏洞和風險前一天通知 PopVote 普及投票及 Civic Data 公民數據負責人。

參考文件   
 [1] 香港電腦保安事故協調中心 [《對 PopVote 普及投票系統資訊保安問題的建議》](https://web.archive.org/web/20210704083525/https://www.hkcert.org/my_url/zh/blog/17020901)   
 [2] [普及投票《個人資料收集聲明》](https://web.archive.org/web/20210704083525/https://cast.popvote.hk/#/pics)   
 [3] [公民數據《保安疑問 Q&A》](https://web.archive.org/web/20210704083525/https://www.facebook.com/CivicDataHK/posts/1806538089597738)

原文刊於 [前線科技人員Facebook專頁](https://web.archive.org/web/20210704083525/https://www.facebook.com/FrontlineTechWorkersConcernGroup/?fref=ts)


---


請加入成為眾新聞的月費訂戶，長期支持我們的工作。所有訂戶都可以收到我們的「每周時事」通訊 。

月費訂戶 [網址：hkcnews.com/aboutus/#subscribe](/web/20210704083525/https://www.hkcnews.com/aboutus/#subscribe)

---

![博客 | 讀者來論](https://web.archive.org/web/20210704083525im_/https://www.hkcnews.com/uploads/avatars/8bd6baf7-e90b-4ec4-be4c-cae03b96fcef.png?1272509898)

**博客 | 讀者來論**

【讀者來論・眾聲】這個專欄開放讀者來論，不設稿酬，稿件請電郵至[email protected]，主旨請註明：投稿【眾聲】。稿件是否採納由《眾新聞》編輯部決定。來稿請說明刊登時採用的名字。
