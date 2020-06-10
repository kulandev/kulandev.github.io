# 如何將 flutter 執行在模擬器與實機上

上一篇文章介紹如何 [建立 flutter 開發環境](../建立flutter開發環境/)，本篇介紹如何將專案執行在 Android、iOS 模擬器與實體機器上

以下操作均以 Mac 操作、VS Code 作為開發工具為主

&nbsp;

## Step 1. 建立 flutter 專案

開啟 VS Code 後，使用快速鍵 cmd + shift + p 或左下小角的設定叫出「命令選擇區」

![term select](https://live.staticflickr.com/65535/49990912541_f86774faec_o.png)

&nbsp;

輸入 flutter

![輸入 flutter](https://live.staticflickr.com/65535/49991170552_49c73e2cc6_b.jpg)

選擇 Flutter: New Project

![Flutter: New Project](https://live.staticflickr.com/65535/49991170552_49c73e2cc6_b.jpg)

輸入希望的專案名稱

![專案名稱](https://live.staticflickr.com/65535/49991170542_c4650f0c7e_b.jpg)

選擇儲存專案的位置

![選擇儲存專案的位置](https://live.staticflickr.com/65535/49991170532_d9588f7ea7_b.jpg)

&nbsp;

即可建立 flutter 專案

![flutter 專案](https://live.staticflickr.com/65535/49990404283_4cb6a9abb5_b.jpg)

{{< admonition tip >}}
圖中的 VS Code 為中文介面與專案 icon 不同，是有安裝以下套件
 - vscode-icons
 - Chinese (Traditional) Language Pack for Visual Studio Code
{{< /admonition >}}

![vscode-icons](https://live.staticflickr.com/65535/49990404278_58cfa9276e_b.jpg)

![Chinese (Traditional) Language Pack for Visual Studio Code](https://live.staticflickr.com/65535/49991170517_1a411af8b7_b.jpg)

## Step 2. 執行在 iOS 模擬器

點選右下角的「No Device」，並選擇「Start iOS Simulator」

![No Device](https://live.staticflickr.com/65535/49990956481_6aa81100dc_b.jpg)

即可開啟 iOS 模擬器

![iOS 模擬器](https://live.staticflickr.com/65535/49991198672_f61d8cabbc_b.jpg)

&nbsp;

{{< admonition tip >}}
若需要其他裝置，例如：iPhone 11、iPhone 11 Pro...，請在 Dock 中的「Simulator」右鍵選擇「Device -> iOS 13.5 -> 你需要的裝置」
{{< /admonition >}}

![其他iOS 模擬器](https://live.staticflickr.com/65535/49990956451_96cdd37bb2_b.jpg)

&nbsp;

{{< admonition tip >}}
如果你需要 iPhone X 或是 iPhone Xs 裝置的話，其實不需要，因為尺寸與iPhone 11 Pro 是相對應的，詳細可參考下圖。

如果需要其他 iOS 版本的模擬器，可以至參考資料的「新增 iPhone 模擬器(simulator)」
{{< /admonition >}}

![iOS解析度對應](https://live.staticflickr.com/65535/49990977811_5b044ca746_b.jpg)

圖片來源：[The Ultimate Guide To iPhone Resolutions](https://www.paintcodeapp.com/news/ultimate-guide-to-iphone-resolutions)

&nbsp;

開啟模擬器後。選擇「執行」，並建立 launch.json 檔案

![建立 launch.json](https://live.staticflickr.com/65535/49991001461_d52b1fd94f_b.jpg)

建立成功，專案會多一個.vscode 檔案夾與 launch.json 檔案

![.vscode 檔案夾與 launch.json 檔案](https://live.staticflickr.com/65535/49991245077_d603beac6f_b.jpg)

回到「執行」，點選左上角綠色箭頭「開始偵錯」，右下角開始進行編譯並將程式跑起來

![開始偵錯](https://live.staticflickr.com/65535/49991011726_c4d2979db1_b.jpg)

編譯完成，將程式寫進模擬器中，完成後會顯示以下的畫面

![iOS 編譯完成](https://live.staticflickr.com/65535/49991245012_b328989335_b.jpg)

&nbsp;

## Setp 3. 執行在 Androd 模擬器

由於還沒有 Android 模擬器，需要先從 Android Studio 中建立 Android 模擬器

![沒有Android 模擬器](https://live.staticflickr.com/65535/49991301842_2542b1375e_b.jpg)

開啟 Android Studio，選擇右下角「Configura -> AVD Manager」

![設定Android模擬器](https://live.staticflickr.com/65535/49991301827_b258150498_b.jpg)

選擇「＋ Create Virtual Device...」

![Create Virtual Device](https://live.staticflickr.com/65535/49990536158_e1fba54a57_b.jpg)

這邊選擇你要的模擬器尺寸

![Virtual Device size](https://live.staticflickr.com/65535/49991301757_450216c498_b.jpg)

選擇該模擬器的 Android 版本，請自行下載需要的版本

![select android version](https://live.staticflickr.com/65535/49990536143_9afc2532cd_b.jpg)

命名 AVD 與確認 AVD 相關資訊後，按下右下角「Finish」建立該 AVD

![check android simulator](https://live.staticflickr.com/65535/49991058141_9976f7fe49_b.jpg)

Android Virtual Device Manager 即出現剛建立完成的 AVD

![check android manager](https://live.staticflickr.com/65535/49990536123_192bc8c2c0_b.jpg)

&nbsp;

回到 VS Code 中，同樣點選點選右下角的「No Device」，出現了剛剛建立的 AVD

![show AVD](https://live.staticflickr.com/65535/49990536118_def05e2b6f_b.jpg)

選擇後，便開啟 Android 模擬器

![open AVD](https://live.staticflickr.com/65535/49990536088_29495f9b56_b.jpg)

同樣回到「執行」，點選左上角綠色箭頭「開始偵錯」，右下角開始進行編譯並將程式跑起來」

![開始偵錯](https://live.staticflickr.com/65535/49990963943_c552ba3718_b.jpg)

編譯完成，將程式寫進模擬器中，完成後會顯示以下的畫面

![Andriod 編譯完成](https://live.staticflickr.com/65535/49991058081_c807f9383c_b.jpg)

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
![open ios/Runner.xcworkspace](https://live.staticflickr.com/65535/49991459227_7cdb79f598_b.jpg)

&nbsp;

輸入完畢，自定打開 Xcode，接著左側的導航面板中選擇 Runner 項目，並選擇「Signing & Capabilities > Team(Add Account...)」

![Signing & Capabilities > Team](https://live.staticflickr.com/65535/49991214391_31acbc1132_b.jpg)

輸入 Apple 開發者帳號

![輸入 Apple 開發者帳號](https://live.staticflickr.com/65535/49991501002_02bacafc00_b.jpg)

確認帳號資訊

![確認帳號資訊](https://live.staticflickr.com/65535/49991255866_666217d90b_b.jpg)

在 Team 選擇 Apple 開發者帳號與修改「Bundle Identifier」

![選擇 Apple 開發者帳號](https://live.staticflickr.com/65535/49991352311_8cef2e453b_o.png)

{{< admonition >}}
Bundle Identifier 是每一個 iOS App 的唯一標識，就像一個人的身份證號碼；必須是唯一值，類似 Android 的 Package name
{{< /admonition >}}

&nbsp;

將 iPhone 與電腦連接，手機會出現是否「信任這部電腦？」

![信任這部電腦？](https://live.staticflickr.com/65535/49991261721_ec6cc6aa7a_o.png)

選擇「信任」後，查看 Xcode 中的裝置列表會出現該手機

![裝置列表](https://live.staticflickr.com/65535/49990734878_2bcd6a2bd0_o.png)

回到「終端機」中輸入下列指令，會看到「連線裝置數」與「裝置詳細狀態」
```Bash
flutter doctor
flutter devices
```
![check devices](https://live.staticflickr.com/65535/49991287911_099e41ea16_b.jpg)

回到 VS Code 會看到，已有連結的手機裝置可以選擇

![已有連結的手機裝置可以選擇](https://live.staticflickr.com/65535/49990789443_b60cf2c132_b.jpg)

選擇手機後，同樣回到「執行」，點選左上角綠色箭頭「開始偵錯」，右下角開始進行編譯並將程式跑起來

![開始偵錯](https://live.staticflickr.com/65535/49991597217_17ca28ac6d_b.jpg)

編譯完成，將程式寫進實機中。後發現開啟應用程式後出現以下畫面

![iOS實體-1](https://live.staticflickr.com/65535/49990860648_036717b824_o.png)

![iOS實體-2](https://live.staticflickr.com/65535/49991381421_b0d1228dcd_o.png)

這時候請至手機中的「設定 -> 一般 -> 裝置管理 -> 該APP」信任該 App

![信任 App](https://live.staticflickr.com/65535/49991626062_2f38113d6b_o.png)

{{< admonition >}}
詳細操作可以參考：[在 iOS 上安裝自定企業 app](https://support.apple.com/zh-tw/HT204460)
{{< /admonition >}}

&nbsp;

信任 App 後，即可進入該 App

![iOS 實機 App](https://live.staticflickr.com/65535/49990875073_c39266a827_b.jpg)


## Setp 5. 執行在 Android 實機

相較於 iOS，Android 要跑在實機中相對簡單多了，只需要準備下列東西就可以了
 - Android 手機一台

&nbsp;

將Android 手機與電腦連線後，Android 手機通常會出現以下畫面，選擇「確定」即可

![Android 實機-1](https://live.staticflickr.com/65535/49991441201_e8663b76e3_b.jpg)

打開手機的開發者模式中的「USB 偵錯」，由於 Android 廠牌眾多，就不逐一介紹如何開啟開發者模式，請自行去針對手機廠牌去 google，通常開啟開發者模式的方法都是在「設定頁面」中的「版本號」連按數下即可開啟

![Android 實機-2](https://live.staticflickr.com/65535/49991684867_6629241d74_b.jpg)

回到 VS Code，會看到已有連結的手機裝置可以選擇

![Android 實機-3](https://live.staticflickr.com/65535/49991684962_2127efc92c_b.jpg)

選擇手機後，同樣回到「執行」，點選左上角綠色箭頭「開始偵錯」，右下角開始進行編譯並將程式跑起來

![Android 實機-4](https://live.staticflickr.com/65535/49991441226_1f6fbe4810_b.jpg)

執行完成，就會自動進入到應用程式的畫面了

![Android 實機-5](https://live.staticflickr.com/65535/49991441146_0a5d793a28_b.jpg)

## Setp 6. 參考資料

 - [新增 iPhone 模擬器(simulator)](https://medium.com/%E5%BD%BC%E5%BE%97%E6%BD%98%E7%9A%84-swift-ios-app-%E9%96%8B%E7%99%BC%E5%95%8F%E9%A1%8C%E8%A7%A3%E7%AD%94%E9%9B%86/%E6%96%B0%E5%A2%9E-iphone-%E6%A8%A1%E6%93%AC%E5%99%A8-simulator-7f5c65a08f97)

 - [Deploy to iOS devices](https://flutter.dev/docs/get-started/install/macos#deploy-to-ios-devices)

- [Set up your Android device](https://flutter.dev/docs/get-started/install/macos#set-up-your-android-device)
