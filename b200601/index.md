# 建立 flutter 開發環境

由於最近手邊的案子需要雙平台，評估了一下 flutter，就來試一下，順便學一個新技能。

以下內容均以 Mac 操作為主。

&nbsp;

## Setp 1. 下載 flutter SDK
下載 [flutter SDK](https://flutter.dev/docs/get-started/install)
{{< admonition >}}
flutter 目前有支援三個作業系統開發，請依照自身環境去下載
{{< /admonition >}}

![flutter Install](https://live.staticflickr.com/65535/49987477231_f9bee9aa47_b.jpg)

&nbsp;

點擊「flutter_macos_1.17.3-stable.zip」並儲存，我的習慣會在根目錄建立一個名為「Dev」的資料夾

![flutter zip](https://live.staticflickr.com/65535/49986963693_452fe844ca_b.jpg)

&nbsp;

## Setp 2. 設定 flutter SDK
解壓縮並設定 flutter SDK path

![unzip](https://live.staticflickr.com/65535/49987771981_6cb4b89dbe_b.jpg)

&nbsp;

打開終端機

![open term](https://live.staticflickr.com/65535/49988019927_e50ba325da_w.jpg)

輸入以下指令
```Bash
code . ~/.bash_profile
```
![input term](https://live.staticflickr.com/65535/49988043787_80a705a1a8.jpg)

{{< admonition tip >}}
code 指令，是 VS Code 的 [Launching from the command line](https://code.visualstudio.com/docs/setup/mac#_launching-from-the-command-line)，請自行安裝
{{< /admonition >}}

&nbsp;

接著將 flutter SDK 路徑填入 .bash_profile 檔案中，讓你可以全域使用 flutter 指令
```Bash
export PATH="$PATH:/Users/{you name}/Dev/flutter/bin"
```
![set flutter SDK](https://live.staticflickr.com/65535/49988126397_048db32d0d_w.jpg)

&nbsp;

儲存後，輸入下列指令，進行套用
```Bash
source ~/.bash_profile
```

&nbsp;

接著輸入 flutter 進行 Building flutter tool
```Bash
flutter
```
![Building flutter](https://live.staticflickr.com/65535/49987904671_fd9381c13a_n.jpg)

&nbsp;

稍等一下，出現下列畫面，即完成 flutter 的安裝

![flutter install end](https://live.staticflickr.com/65535/49988152822_89be53f459_c.jpg)

&nbsp;

接著執行 flutter doctor，會幫你檢查你電腦還 __「缺少」__ 什麼東西
```Bash
flutter doctor
```
![flutter doctor](https://live.staticflickr.com/65535/49988005696_1cbf818803_b.jpg)

&nbsp;

## Setp 3. 安裝開發工具 - VS Code

flutter 的開發工具主要有兩個，一個是 [VS Code](https://code.visualstudio.com/)，另一個是 Android Studio，VS Code 安裝過程很簡單，就不逐步介紹了，VS Code 還需要下列兩個套件軟體，請自行去 VS Code extension marketplace 下載安裝
 - Flutter
 - Dart

![flutter vs code ext](https://live.staticflickr.com/65535/49987938026_1c36001635_b.jpg)
![Dart vs code ext](https://live.staticflickr.com/65535/49987423793_b5a0660d1d_b.jpg)

&nbsp;

## Setp 4. 安裝開發工具 - Android Studio

Flutter 是由 Google 開發的開源行動應用軟體開發套件，因此也整合至自家的 [Android Studio](https://developer.android.com/studio) 中，要透過 flutter 開發 Android，還有需要 Android SDK 與 AVD(Android Virtual Devices) 模擬器，因此需要安裝 Android Studio。

&nbsp;

請自行安裝與設定，Android Studio 安裝過程網路上有許多教學，就不逐步介紹了，完成開啟後，請選擇右下角的「Configure -> Plugins」，安裝 flutter Plugins，安裝完畢後，初始頁面會增加一個建立 flutter 專案的選項

![Configure](https://live.staticflickr.com/65535/49987553658_54334ab782_b.jpg)
![flutter Plugins](https://live.staticflickr.com/65535/49987553673_030d1c4037_b.jpg)
![Configure](https://live.staticflickr.com/65535/49988083996_1b924cfc56_b.jpg)

&nbsp;

## Setp 5. 安裝開發工具 - Xcode

Flutter 需要開發 iOS，安裝 Xcode 也是必不可少的，請自行去 App Store 進行安裝，安裝完成，開啟並執行「同意」等操作

{{< admonition warning >}}
安裝完成，務必開啟 Xcode 進行相關「同意」設定
{{< /admonition >}}

![Xcode](https://live.staticflickr.com/65535/49988045516_598784349f_b.jpg)

&nbsp;

## Setp 6. 再次檢測 flutter doctor

再次執行 flutter doctor
```Bash
flutter doctor
```
顯示還缺少兩項，就依照說明逐一執行即可

![flutter doctor again](https://live.staticflickr.com/65535/49987607668_5433188a50_b.jpg)

&nbsp;

Andorid：執行下列指令，並會需要你選擇 y 同意即可
```Bash
flutter doctor --android-license
```

iOS：執行下列指令
```Bash
sudo gem install cocoapods
pod setup
```

&nbsp;

執行完畢後，再次執行 flutter doctor，若出現下面畫面，表示 flutter 完成安裝

![flutter install over](https://live.staticflickr.com/65535/49988397502_8b64b16e2d_b.jpg)

{{< admonition question >}}
 Connected device 會出現驚嘆號的原因在於，沒有開啟任何模擬器與連接實機(iOS、Android)
{{< /admonition >}}

&nbsp;

## Setp 7. 參考資料

 - [Flutter install 官方文件](https://flutter.dev/docs/get-started/install)
