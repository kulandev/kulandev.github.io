# 如何在 Google Domains 購買網域 + Github Page 設定

最近開始寫 Blog，也順便學一下如何購買 Domains 與設定。

購買網域，國內外都有很多管道可以選擇，但這篇是在 Google Domains 上買，為什麼選擇 Google Domains，原因在於有一些特殊網域可以選擇「例如：dev、app...等」，外加每年的費用一致，不像 go****，頭一年超便宜，之後續約開始漲價，但 Google Domains 的缺點就是不支援「.tw、com.tw」結尾的網域，所以要選擇麼哪家的網域商自行斟酌囉

![L9oFLIe](https://i.imgur.com/L9oFLIe.png)

![YPRRHWh](https://i.imgur.com/YPRRHWh.png)

&nbsp;

## Step 1. Google Domains 購買網域

前往 [Google Domains](https://domains.google.com/m/registrar/search?hl=zh-TW) 搜尋你要的網域

![zkl5EFQ](https://i.imgur.com/zkl5EFQ.png)

{{< admonition tip >}}
上方雖然顯示「Google Domains 尚未於您所在國家/地區推出。 」，但實際上還是可以購買使用的
{{< /admonition >}}

會依照你搜尋的網域。來決定每年的價格，如果你搜尋的網域已經有人購買的，也會出現其他的建議名稱

![7uM5O8F](https://i.imgur.com/7uM5O8F.png)

選定好網域之後，直接加入購物車進行購買

![JSfU7ut](https://i.imgur.com/JSfU7ut.png)

進行「結帳」時，會發現「選取帳單或法定國家/地區」沒有台灣可以選擇，但這邊直接選擇「美國」是可以的。

![GPTphn8](https://i.imgur.com/GPTphn8.png)

接著會請你輸入聯絡資訊，國家區域可以選擇「台灣」
![hpkrbtA](https://i.imgur.com/hpkrbtA.png)

請在依序填入聯絡資訊並儲存，接著刷卡結帳即可完成購買網域

{{< admonition warning >}}
有稍微要注意的一點是，假設我的地址：110台北市信義區信義路五段7號
「市」的欄位其實是要填「區」的資訊。例如：信義區，這樣才可以儲存聯絡資訊，應該是網站翻譯的問題
{{< /admonition >}}

![yoiXNxC](https://i.imgur.com/yoiXNxC.png)

![89cxORg](https://i.imgur.com/89cxORg.png)

&nbsp;

## Step 2. Github Page 設定網域

在 blog github Settings 頁面中找到「GitHub Pages -> Custom domain」填入剛剛購買的網域

![D2EEmI2](https://i.imgur.com/D2EEmI2.png)

![B66jNFs](https://i.imgur.com/B66jNFs.png)

&nbsp;

## Step 3. Google Domains 設定 DNS

回到 Google Domains 進入 DNS 頁面中的「自訂資源記錄」
分別新增兩組資訊
{{< admonition tip >}}

一組類型：「A」資料：如下，作用為指向 Github IP
 - 185.199.108.153
 - 185.199.109.153
 - 185.199.110.153
 - 185.199.111.153

一組名稱：「www」;類型：「CNAME」;資料：「{you blog}.github.io」
{{< /admonition >}}
![kRMp2K8](https://i.imgur.com/kRMp2K8.png)

設定完成後，需要等它對應完成，至於要多久，我也不知道，我是等了10多分鐘左右

{{< admonition warning >}}
記得回到 「GitHub Pages -> Custom domain」將「Enforce HTTPS 」給打勾
{{< /admonition >}}

![DgwbSEr](https://i.imgur.com/DgwbSEr.png)

&nbsp;

## Step 4. 參考資料

 - [Google Domains 台灣可以使用了﹍購買 + 轉移網域(Godaddy) + DNS 設定心得](https://www.wfublog.com/2019/04/google-domains-tw-purchase-transfer-godaddy-dns.html)

 - [Managing a custom domain for your GitHub Pages site](https://help.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site#configuring-a-records-with-your-dns-provider)

 - [GitHub Pages and Google Domains together](https://dev.to/brunodrugowick/github-pages-and-google-domains-together-5ded)
