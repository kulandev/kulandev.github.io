# 如何將 flutter 執行在模擬器與實機上

上一篇文章介紹如何 [建立 flutter 開發環境](../建立flutter開發環境/)，本篇介紹如何將專案執行在 Android、iOS 模擬器與實體機器上

以下操作均以 Mac 操作、VS Code 作為開發工具為主

&nbsp;

## Step 1. 建立 flutter 專案

開啟 VS Code 後，使用快速鍵 cmd + shift + p 或左下小角的設定叫出「命令選擇區」

![uL3jthy](https://i.imgur.com/uL3jthy.png)

&nbsp;

輸入 flutter，選擇 Flutter: New Project

![u0NLe4v](https://i.imgur.com/u0NLe4v.png)

輸入希望的專案名稱

![VthhR2m](https://i.imgur.com/VthhR2m.png)

選擇儲存專案的位置

![43Qruin](https://i.imgur.com/43Qruin.png)

&nbsp;

即可建立 flutter 專案

![fyFXS5q](https://i.imgur.com/fyFXS5q.png)

{{< admonition tip >}}
圖中的 VS Code 為中文介面與專案 icon 不同，是有安裝以下套件
 - vscode-icons
 - Chinese (Traditional) Language Pack for Visual Studio Code
{{< /admonition >}}

![xlFgE99](https://i.imgur.com/xlFgE99.png)

![OKVKpyk](https://i.imgur.com/OKVKpyk.png)

## Step 2. 執行在 iOS 模擬器

點選右下角的「No Device」，並選擇「Start iOS Simulator」

![vh2Amhq](https://i.imgur.com/vh2Amhq.png)

即可開啟 iOS 模擬器

![2YjFUId](https://i.imgur.com/2YjFUId.jpg)

&nbsp;

{{< admonition tip >}}
若需要其他裝置，例如：iPhone 11、iPhone 11 Pro...，請在 Dock 中的「Simulator」右鍵選擇「Device -> iOS 13.5 -> 你需要的裝置」
{{< /admonition >}}

![OEkYEjj](https://i.imgur.com/OEkYEjj.png)

&nbsp;

{{< admonition tip >}}
如果你需要 iPhone X 或是 iPhone Xs 裝置的話，其實不需要，因為尺寸與iPhone 11 Pro 是相對應的，詳細可參考下圖。

如果需要其他 iOS 版本的模擬器，可以至參考資料的「新增 iPhone 模擬器(simulator)」
{{< /admonition >}}

![WdPyHdT](https://i.imgur.com/WdPyHdT.png)

圖片來源：[The Ultimate Guide To iPhone Resolutions](https://www.paintcodeapp.com/news/ultimate-guide-to-iphone-resolutions)

&nbsp;

開啟模擬器後。選擇「執行」，並建立 launch.json 檔案

![mvitHTZ](https://i.imgur.com/mvitHTZ.png)

建立成功，專案會多一個.vscode 檔案夾與 launch.json 檔案

![T0oklFK](https://i.imgur.com/T0oklFK.png)

&nbsp;

回到「執行」，點選左上角綠色箭頭「開始偵錯」，右下角開始進行編譯並將程式跑起來

![gIpiTop](https://i.imgur.com/gIpiTop.png)

編譯完成，將程式寫進模擬器中，完成後會顯示以下的畫面

![qHzFeDl](https://i.imgur.com/qHzFeDl.jpg)

&nbsp;

## Setp 3. 執行在 Androd 模擬器

由於還沒有 Android 模擬器，需要先從 Android Studio 中建立 Android 模擬器

![J2v5Wi0](https://i.imgur.com/J2v5Wi0.png)

開啟 Android Studio，選擇右下角「Configura -> AVD Manager」

![40EVh62](https://i.imgur.com/40EVh62.jpg)

選擇「＋ Create Virtual Device...」

![oDnSJdP](https://i.imgur.com/oDnSJdP.png)

這邊選擇你要的模擬器尺寸

![I0cO7MY](https://i.imgur.com/I0cO7MY.png)

選擇該模擬器的 Android 版本，請自行下載需要的版本

![ZnBGjP4](https://i.imgur.com/ZnBGjP4.png)

命名 AVD 與確認 AVD 相關資訊後，按下右下角「Finish」建立該 AVD

![m1AUOKS](https://i.imgur.com/m1AUOKS.png)

Android Virtual Device Manager 即出現剛建立完成的 AVD

![Pnvk9YC](https://i.imgur.com/Pnvk9YC.png)

&nbsp;

回到 VS Code 中，同樣點選點選右下角的「No Device」，出現了剛剛建立的 AVD

![8RRvCw4](https://i.imgur.com/8RRvCw4.png)

選擇後，便開啟 Android 模擬器

![U8Zz9V0](https://i.imgur.com/U8Zz9V0.jpg)

同樣回到「執行」，點選左上角綠色箭頭「開始偵錯」，右下角開始進行編譯並將程式跑起來」

![AvdU5AX](https://i.imgur.com/AvdU5AX.png)

編譯完成，將程式寫進模擬器中，完成後會顯示以下的畫面

![JmPZihp](https://i.imgur.com/JmPZihp.jpg)

&nbsp;

## Setp 4. 執行在 iOS 實機

要將程式執行在 iOS 實機上，需要準備以下的東西
 - [Apple 開發者帳號](https://developer.apple.com/programs/)(可以先不繳交年費)
 - iPhone 一台
 - 安裝 cocoapods
 - 安裝 Xcode

&nbsp;

打開「終端機」，透過 cd 指令，進入到剛剛建立的 flutter 專案，並在專案底下輸入「open ios/Runner.xcworkspace」，參考如下

```Bash
cd Dev/App/{you flutter project name}
open ios/Runner.xcworkspace
```
![YJosB9X](https://i.imgur.com/YJosB9X.png)

&nbsp;

輸入完畢，自定打開 Xcode，接著左側的導航面板中選擇 Runner 項目，並選擇「Signing & Capabilities > Team(Add Account...)」

![C3K4g5X](https://i.imgur.com/C3K4g5X.jpg)

輸入 Apple 開發者帳號

![jtw1xmy](https://i.imgur.com/jtw1xmy.png)

確認帳號資訊

![wpEgtxz](https://i.imgur.com/wpEgtxz.png)

在 Team 選擇 Apple 開發者帳號與修改「Bundle Identifier」

![CeCcN7d](https://i.imgur.com/CeCcN7d.png)

{{< admonition >}}
Bundle Identifier 是每一個 iOS App 的唯一標識，就像一個人的身份證號碼；必須是唯一值，類似 Android 的 Package name
{{< /admonition >}}

&nbsp;

將 iPhone 與電腦連接，手機會出現是否「信任這部電腦？」

![DO9jbcH](https://i.imgur.com/DO9jbcH.png)

選擇「信任」後，查看 Xcode 中的裝置列表會出現該手機

![CGF2q2T](https://i.imgur.com/CGF2q2T.png)

回到「終端機」中輸入下列指令，會看到「連線裝置數」與「裝置詳細狀態」
```Bash
flutter doctor
flutter devices
```
![qH4050i](https://i.imgur.com/qH4050i.png)

&nbsp;

回到 VS Code 會看到，已有連結的手機裝置可以選擇

![EJ7AGdD](https://i.imgur.com/EJ7AGdD.png)

選擇手機後，同樣回到「執行」，點選左上角綠色箭頭「開始偵錯」，右下角開始進行編譯並將程式跑起來

![2dMCgc3](https://i.imgur.com/2dMCgc3.png)

&nbsp;

編譯完成，將程式寫進實機中。後發現開啟應用程式後出現以下畫面

![gmfQrE2](https://i.imgur.com/gmfQrE2.png)

![A1ncHye](https://i.imgur.com/A1ncHye.png)

這時候請至手機中的「設定 -> 一般 -> 裝置管理 -> 該APP」信任該 App

![ptJZT5O](https://i.imgur.com/ptJZT5O.png)

{{< admonition >}}
詳細操作可以參考：[在 iOS 上安裝自定企業 app](https://support.apple.com/zh-tw/HT204460)
{{< /admonition >}}

&nbsp;

信任 App 後，即可進入該 App

![vb6M06f](https://i.imgur.com/vb6M06f.jpg)

## Setp 5. 執行在 Android 實機

相較於 iOS，Android 要跑在實機中相對簡單多了，只需要準備下列東西就可以了
 - Android 手機一台

&nbsp;

將Android 手機與電腦連線後，Android 手機通常會出現以下畫面，選擇「確定」即可

![oGIDfml](https://i.imgur.com/oGIDfml.jpg)

打開手機的開發者模式中的「USB 偵錯」，由於 Android 廠牌眾多，就不逐一介紹如何開啟開發者模式，請自行去針對手機廠牌去 google
{{< admonition >}}
通常開啟開發者模式的方法都是在「設定頁面」中的「版本號」連按數下即可開啟
{{< /admonition >}}

![gqehTxg](https://i.imgur.com/gqehTxg.png)

&nbsp;

回到 VS Code，會看到已有連結的手機裝置可以選擇

![JWAyjW5](https://i.imgur.com/JWAyjW5.png)

選擇手機後，同樣回到「執行」，點選左上角綠色箭頭「開始偵錯」，右下角開始進行編譯並將程式跑起來

![C2heeim](https://i.imgur.com/C2heeim.png)

執行完成，就會自動進入到應用程式的畫面了

![8XtxSux](https://i.imgur.com/8XtxSux.jpg)

## Setp 6. 參考資料

 - [新增 iPhone 模擬器(simulator)](https://medium.com/%E5%BD%BC%E5%BE%97%E6%BD%98%E7%9A%84-swift-ios-app-%E9%96%8B%E7%99%BC%E5%95%8F%E9%A1%8C%E8%A7%A3%E7%AD%94%E9%9B%86/%E6%96%B0%E5%A2%9E-iphone-%E6%A8%A1%E6%93%AC%E5%99%A8-simulator-7f5c65a08f97)

 - [Deploy to iOS devices](https://flutter.dev/docs/get-started/install/macos#deploy-to-ios-devices)

- [Set up your Android device](https://flutter.dev/docs/get-started/install/macos#set-up-your-android-device)
